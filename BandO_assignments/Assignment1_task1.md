Assignment 1
**************

Task 1:

Following clarifications required from the development team:
- Firmware compatability to the feature- Minimum firmware required to enable this feature. Error handling if the FW does not support
- What is definition of connected - Is it when primary earbud connected or when both connected?
- Course of action if time taken to change the mode > 2ms - error or retry ?
If retry, how many are allowed. What is the error handling mechanism if it fails.
- How to determine if mode change is success - Is there any feedback from device and is there any display message on app. Is there any way to query device mode for testing purpose
- What is app behavior when mode change is not allowed(  disconnected / low battery) - adaptive listening mode button grayed out or error message displayed on attempting to change?
- What should be expected behavior if any disconnection happens during switch - Is the request to change aborted or will be reattempted?
- Is mode change possible from device. if yes, what has more priority - app or device?
- Behavior during phone call - Is mode locked during call. What happens if mode change attempted during call?
- What device is considered for determining battery level - primary earbud or both ?
- Is 2s a strict requirement or is there any acceptable deviation in high interference scenario?
- Where is last selected mode stored - device or app memory? if in device, is it persistent when a new phone is connected to device.
- Is there any dependencies for iOS and Android versions

Assumptions :
- Device will be source of truth for the active mode.
- Battery status is reported real time from device to app.
- All software and firmware components build will be available with feature functionally complete.
- Test team is provided with all necessary requirement documents and design/functional specification documents on time for test planning, designing and execution.

Critical Risks:
- App shows one mode and device has another mode active.
Test strategy: Initate mode change from app and verify it on device. Need a mechanism to query device state after initiating mode change from the app.

- FW mismatch - If the FW doesnot support feature and app tries to change the mode, it can lead to crash or silent failures which can result in loss of reliability from the user. 
Test strategy: Multi-firmware matrix testing on both platforms

- Bluetooth connection quality variation in real environments which can impact the latency spec (2s) in different environments. This need a mechanism for multiple attempts to mitigate this risk and acceptable deviation from the 2ms requirement under high interference environments.
Test strategy: Test the mode change in different envrionments and make a performance comparison.

- Difference in behavior across iOS and android.
Test strategy : Multi platform testing and across a good mix of phone models to address hardware dependencies.

- Error in battery level reported from app. It can be due to long gap between battery status queries from app. 
Test strategy : Verify the battery level reported from app is matching to actual device values

- Mode status is not persistent after app crash/update/restart.
Test strategy : Simulate app crash/update/restart and verify values before and after

- Mode change initiated during a call resulting in unexpected failures like call drops
Test strategy : Test mode switching during a call.

 
