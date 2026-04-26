Assignment 1
**************

Task 7:

I would go for conditional release.

- Issue 1: Android SLA deviation (Moderate)
This is an intermittent performance issue and does not break core functionality, so it should not block release.

However, I would proceed only if:

The deviation stays within an acceptable threshold (low frequency, no extreme delays)
Documentation is included in the release notes indicating performance deviation
Product/marketing teams are aligned on SLA expectations for Android

- Issue 2: UX wording (Low)
This has no functional impact and is low effort. Ideally, it should be fixed before release.
If timelines are tight, it is safe to include in a near-term patch.

- Issue 3: Mode mismatch after reconnect (Critical)
This impacts the reliability of the feature and must be addressed before release. This issue breaks the expectation that the app reflects the actual device state, which is critical for a premium product experience. 

At minimum, we need:

A mitigation ensuring the app does not persist incorrect state. App should re-fetch or validate device state on reconnect/app resume and correct any mismatch.

If only a partial fix is possible:

Ensure the app reflects the device state on reconnect or app resume.
Perform focused testing on reconnection scenarios.
With mitigation in place, a conditional release is acceptable, followed by a high-priority patch.