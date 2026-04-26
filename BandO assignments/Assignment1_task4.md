Assignment 1
**************

Task 4:

1. Switch the mode from app and verify that mode is reflected on device .
TC ID     : xxx
Feature   : Adaptive listening mode
Test type : Functional
Platform  : IOS, Android
Complexity : Medium

Prerequisites:
- Device is paired with the app.
- Earbud is connected (bluetooth shows connected)
- FW version > vx.x
- Battery level > 20%
- Audio is playing

Steps	|  Expected result
1. Open the app and check if device is displayed in the app	|  App shows the device info(connection status, battery info etc)
2. Verify the app shows current mode as indicated from audio perception	|  Current mode displayed matches with value inferred from audio perception
3. Click on button ‘Adaptive listening mode’   | 	Button displays 2 options – noise cancellation , transparency
4. Switch the mode to transparency mode  |  Message is displayed as ‘Switched to transparency mode*; No error/ crash observed
5. Verify app is showing transparency mode in the device info  |	App displays transparency mode in device info
6. Verify that the state on device is transparency mode   | 	Device has transparency mode 
7. Verify mode is actually transparency from audio perception	|  Audio perception implies transparency mode
8. Audio drop is not observed during the switch
9. Repeat  steps 4-8 for Noise cancellation mode.


Pass/Fail Criteria:
- Pass criteria:  Mode switch is successful and is reflecting correctly in both device and app. No error message/crash observed. No audio drops observed. 
- Fail criteria: Modes are not reflected correctly in app/ device. App crashes/ error message shown. Audio drops observed.



2. Verify the mode is restored after reconnect.

TC ID     : xxx
Feature   : Adaptive listening mode
Test type : Functional
Platform  : IOS, Android
Complexity : Medium

Prerequisites:
- Device is paired with the app.
- Earbud is connected (bluetooth shows connected)
- FW version > vx.x
- Battery level > 20%
- Audio is playing

Steps	|  Expected result

1. Open the app and check if device is displayed in the app	|  App shows the device info(connection status, battery info etc)
2. Verify the app shows current mode as indicated from audio perception	|  Current mode displayed matches with value inferred from audio perception
3. Switch the mode from app | Mode switch is successful; No error message displayed.
4.  Disconnect earbuds (earbuds removed or go out of range)
5. Verify the status in device info  | Device status is 'Disconnected'
6. Reconnect device   | Device reconnected successfully and device status on app shows connected.
7. Check the active mode displayed on app | Active mode displayed is the last selected mode
8. Verify the mode from device and from audio perception |  Mode on device and from audio perception matches the last selected mode.
9. Repeat steps 3-8 for transparency / Noise cancellation mode

Pass/Fail Criteria:
- Pass criteria:  Mode switch is successful and is reflecting correctly in both device and app. Last selected mode is restored after reconnection.
- Fail criteria: Modes are not reflected correctly in app/ device. App crashes/ error message shown. Last selected mode is not restored after reconnection





