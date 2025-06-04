# Onboarding with Improv-BLE

After initial power-up or a factory reset, the device will enter onboarding mode for 10 minutes.

## How to Onboard

> **Note:**
> - If your device has already been onboarded before, go to **Settings → Devices & Services → ESPHome** in Home Assistant and delete the device from the list before starting the onboarding process again.
> - The **Improv via BLE** option may also appear in Home Assistant if you are running Bluetooth proxies, but using the web interface to onboard the device will most likely fail.

1. **Open the Home Assistant Companion App**
   Make sure Bluetooth is enabled on your mobile device.

2. **Go to:**
   **Settings → Devices & Services**

   <a href="onboarding/rowi-mobile-ble-1.png" target="_blank">
     <img src="onboarding/rowi-mobile-ble-1.png" alt="Onboarding step 1" width="200">
   </a>
   <a href="onboarding/rowi-mobile-ble-2.png" target="_blank">
     <img src="onboarding/rowi-mobile-ble-2.png" alt="Onboarding step 2" width="200">
   </a>
   <a href="onboarding/rowi-mobile-ble-3.png" target="_blank">
     <img src="onboarding/rowi-mobile-ble-3.png" alt="Onboarding step 3" width="200">
   </a>
   <a href="onboarding/rowi-mobile-ble-4.png" target="_blank">
     <img src="onboarding/rowi-mobile-ble-4.png" alt="Onboarding step 4" width="200">
   </a>

   After WiFi is connected, the device will also be discovered in Home Assistant and can be added from the web interface.

   <a href="onboarding/rowi-mobile-ble-5.png" target="_blank">
     <img src="onboarding/rowi-mobile-ble-5.png" alt="Onboarding step 5" width="200">
   </a>
   <a href="onboarding/rowi-mobile-ble-6.png" target="_blank">
     <img src="onboarding/rowi-mobile-ble-6.png" alt="Onboarding step 6" width="200">
   </a>
   <a href="onboarding/rowi-mobile-ble-7.png" target="_blank">
     <img src="onboarding/rowi-mobile-ble-7.png" alt="Onboarding step 7" width="200">
   </a>
   <a href="onboarding/rowi-mobile-ble-8.png" target="_blank">
     <img src="onboarding/rowi-mobile-ble-8.png" alt="Onboarding step 8" width="200">
   </a>

3. **View your onboarded device in ESPHome:**
   Go to **Settings → Devices & Services → ESPHome** to see your device listed.

   <a href="onboarding/rowi-mobile-ble-9.png" target="_blank">
     <img src="onboarding/rowi-mobile-ble-9.png" alt="Onboarding step 9" width="200">
   </a>

---

## Troubleshooting

- Ensure Bluetooth is enabled on your mobile device.
- Make sure the device is powered and in onboarding mode (after initial power-up or factory reset).
- If the device is not discovered, try restarting the device or the Home Assistant app.
- If onboarding mode times out, power cycle or factory reset the device to re-enter onboarding mode.



