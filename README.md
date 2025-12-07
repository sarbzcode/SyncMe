# Sync Audio Prototype

A runnable prototype that keeps audio playback synchronized between an iPhone and an iPad over Wi-Fi. One device becomes the host and broadcasts timestamps so clients stay aligned.

## Setup

1. Install Node.js 18+.
2. Install dependencies:
   ```bash
   npm install
   ```

## Run

```bash
npm start
```

The server starts on port 8080 and prints your LAN URLs.

## Use on iPhone/iPad

1. Connect both devices to the same Wi-Fi network.
2. From each device, open the printed LAN URL (e.g., `http://192.168.1.20:8080`).
3. On one device, tap **Become Host**.
4. On both devices, choose the same local audio file via the file picker.
5. Press play on the host if needed—the client auto-syncs.

## Testing Steps

1. Run `npm install`.
2. Run `npm start`.
3. Open `http://<LAN-IP>:8080` on both devices.
4. On one device, become host and play the audio.
5. On the second device, select the same audio file; it will sync automatically.
