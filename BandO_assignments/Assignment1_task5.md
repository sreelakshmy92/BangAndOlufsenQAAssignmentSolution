Assignment 1
**************

Task 5:

Bug title : Mode status info on UI does not match the actual device state

Description:  When the user selects a listening mode (e.g., Transparency Mode) in the mobile app while earbuds are connected, the app immediately updates its UI to display the newly selected mode as active. However, the earbuds remain in the previous mode (e.g., Noise Cancellation) for 8–12 seconds. In some cases, after the user places earbuds back in the charging case and reconnects them, the app continues to show the user's last selected mode, but the earbuds reconnect in a different mode (the mode from before the user's change attempt), leaving app and device state misaligned.

Steps to reproduce:
Scenario 1:
1. Open mobile app and verify if device is connected and play some audio.
2. Verify current mode is noise cancellation. Confirm this from audio perception.
3. Switch mode to transparent - app displays transparency mode immediately
4. Verify device mode - it will show noise cancellation. Confirm this from audio perception.
App mode - Transparency , device mode - NC
Scenario 2:
1. Open mobile app and verify if device is connected and play some audio.
2. Verify current mode is noise cancellation. Confirm this from audio perception.
3. Switch mode to transparent - app displays transparency mode immediately
4. Place the earbuds in case within 8s - confirm app shows status as disconnected
5. Reconnect the device after 10 s - confirm app shows status as connected and active mode as transparency.
6. Verify device mode - it will show noise cancellation. Confirm this from audio perception.
App mode - Transparency , device mode - NC

Expected result:
App should not change value without a confirmation from the device. Values from app and device should match.
Mode change should take place within 2s ( can be tracked by separate bug) 
After reconnect, correct mode should be restored and displayed.

Actual result:
App changes value immediately without checking device state. 
Device takes >8s to change mode.
After reconnection, app is not querying the device state before displaying previous value and also no attempt to restore the mode to requested one.

Impact:
Core feature expectation is broken

- FW version :
- App version:
- OS : Observed in iOS (version), android (version)
- earbud model:
- Phone model:
- Severity : High
- Priority : Showstopper
- Reproducibility: High(consistent)
- Attachments : Device logs, app logs, screen recordings for the failures



