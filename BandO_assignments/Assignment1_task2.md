Assignment 1
**************

Task 2:

- what you would test first and why
1. Basic sanity check - Device is able to be paired and app shows the connection status (on/off)reliably. 
Battery level is reported in app and corresponds to actual values on device. These are basic sanity cases to be checked initially and required for the feature to work.
2. Happy path testing - Connect device to app. Initiate mode switch. Verify mode is changed on device within 2ms. Verify that app and device are in sync w.r.t mode. Repeat this testcase for switching from transparent to Noise cancellation and vice versa. This test would cover the basic feature functionality.

- what areas would you prioritize most
Below will be prioritization areas as these are high risk areas and can impact user perception.
1. State sync between device and app
2. State restoration after reconnect 
3. Consistency across IOS and Android
4. Handling unsupported FW
5. SLA verification within different environments
6. Persistence after app crash/update
7. Mode change initiated during call
8. Mode change during low battery scenarios

- what you would focus on in exploratory testing
1. Stress test - Rapid connect/disconnect, Rapid mode switches
2. SLA comparison for mode change in different real world scenarios - open areas, office, crowded areas, bus/train etc
3. Device disconnected in between switch
4. Verify low battery scenario left earbud only, right earbud only, both earbuds , case only etc.
5. Connect a new phone to device and verify if the mode reported from app is correct.
6. Verify the scenario when headset is connected to both laptop and phone.
7. Verification at the edge of Bluetooth range(distance between headset and phone is nearing the max range) and error handling on app when mode switch is initiated if device just went out of range.
8. FW compatability and platform compatability matrix
9. What happens if app is backgrounded or killed during switch
10. Audio -> call transition during switch (incoming call)
11. Boundary value testing around 5% battery

- what regression areas would you consider important
1. Basic bluetooth pairing/unpairing
2. Switching from case/device still works(if they already exist)
3. Any drop in audio playback or calls
4. Battery reporting on app and battery usage pattern
5. App memory usage

- how you would think about coverage across iOS and Android?

Test have to be run on IOS and Android as the Bluetooth flows will be different and single platform validation will not be sufficient. Tests should also consider the features supported by the BLE stack of individual OS -eg:  if there are any features or paths suupported only in IOS. Also, it will be better if testing is distributed across 2-3 device manufacturers and multiple versions of OS(N, N-1 and N-2 - to be decided from historic data)
