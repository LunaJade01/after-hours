# After Hours — iPad web app

This is an experimental local-first prototype for Safari on iPad.

## Publish
1. Create a new **public** GitHub repository named `after-hours`.
2. Upload `index.html`, `manifest.webmanifest`, and `sw.js` to the repository root.
3. In GitHub, open **Settings → Pages**.
4. Under Build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. Wait for GitHub Pages to publish. Your site URL will be shown in Settings → Pages.

## Use on iPad
1. Open the published URL in Safari on your iPad.
2. Tap Share → Add to Home Screen.
3. Open the app and visit **AI setup → Download & start local AI**.
4. Keep Safari open and on Wi-Fi during the first model download.

## Important limitations
- The prototype uses WebLLM and WebGPU in Safari. It requires a compatible iPadOS/Safari build (WebGPU support is required; iPadOS 26+ is recommended).
- Model availability and performance on the standard A16 iPad are not guaranteed. If WebGPU/model initialization fails, it will show an error rather than use a paid or remote AI API.
- Model weights are downloaded from a public CDN on first use. The initial download requires internet access. Subsequent model caching depends on Safari storage policies.
- Character profiles and chat history are stored in this browser's local storage. Clearing Safari website data can erase them. Export a backup in Settings.
- GitHub Pages hosts the static files for free; it does not run the AI.
- This prototype does not implement background/initiated messages, cloud sync, or cross-device memory.
