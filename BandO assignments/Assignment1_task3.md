Assignment 1
**************

Task 3:

High value test scenarios:

1. Switch the mode from app and verify that value on app and device matches. Perform the test from NC -> transparent and vice versa. Verify that mode is actually changed from audio perception.
2. Verify that mode cannot be changed when device is disconnected.
3. Mode restored after device is reconnected.
4. Mode switching is blocked when battery level is less than 5% and expected message is displayed.
5. Verify mode is restored after app restart.
6. Verify that battery level displayed on app matches to actual values on device.
7. Verify the app behavior with unsupported FW - is app handling it gracefully
8. Verify the SLA is within acceptable limits in multiple real world scenarios and across IOS/Android versions.
9. verify the mode switching behavior during call  and audio playback
10. Stress scenarios - 1) disconnect/reconnect scenario for 20 times and verify mode is correctly set each time 2) Rapid mode switches 



