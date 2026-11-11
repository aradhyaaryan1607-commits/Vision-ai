# VisionAI

Live obstacle detection with voice alerts. Works with a phone camera or an ESP32-CAM stream.

- Detects objects, draws a labelled box, estimates distance, and says e.g. "chair ahead, 1 metre".
- Runs fully in the browser (TensorFlow.js + COCO-SSD). No server needed.

## Host on GitHub Pages
1. Create a new repo, upload `index.html` and this README.
2. Settings → Pages → Deploy from a branch → `main` / root → Save.
3. Open `https://<your-username>.github.io/<repo>/` on your phone.

## ESP32-CAM
Flash the CameraWebServer example. Use the stream address `http://<ESP-IP>:81/stream`.
Phone and ESP32-CAM must be on the same Wi-Fi.
GitHub Pages is https and the ESP32 is http, so allow "Insecure content" for the site in browser settings
(Chrome: site settings → Insecure content → Allow), or open `index.html` locally.

## Notes
Distance is an estimate from object size. Adjust "Camera view angle" to calibrate. Do not rely on it as a safety device.
