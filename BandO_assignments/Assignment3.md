Assignment 3
**************

- Device 1 is identified as the primary earbud because log contains:

1. HFP (Hands-Free Profile), A2DP (Advanced Audio Distribution Profile), AVRCP (Audio/Video Remote Control Profile) protocols
2. Multipoint connectivity, as it is connected simultaneously to an iPhone (68:ef:dc:db:3d:8e) and an Intel Bluetooth adapter (04:f0:ee:09:c3:be)

These capabilities indicate that Device 1 manages the full Bluetooth audio stack and acts as the main audio endpoint.

- Device 2 is identified as the secondary earbud because:

1. No HFP, A2DP, or AVRCP signaling is observed
2. However, it shows significant traffic, indicating active participation
3. It interacts with the case and other devices

- Device 3 is identified as the charging case because:

1. Explicit device name: “Beo Grace Case”
2. Uses BLE protocols (ATT, SMP) including pairing procedures
3. No audio-related profiles (HFP/A2DP/AVRCP) are present

User Scenario:

The earbuds are connected simultaneously to a laptop (Intel Bluetooth) and an iPhone, demonstrating multipoint connectivity
The user:
switches between audio playback and calls
pauses and resumes audio playback
performs volume adjustments
AVRCP logs confirm playback control (e.g., play/pause events and status changes)
HFP logs confirm call-related signaling.