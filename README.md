# Param AI Studio

An iPad-friendly static web app for local AI chat and optional cloud video generation.

## Run
Open via a local HTTP server or deploy the three app files (`index.html`, `style.css`, `app.js`) to GitHub Pages. The model requires an initial download. Internet access is also needed to load the Transformers.js library unless you bundle it locally. Offline operation after caching is **not guaranteed** on iPad Safari.

## AI chat
Uses Transformers.js and `Xenova/flan-t5-small` with WASM inference. It is a small instruction model, not comparable to modern cloud chat models. Memory limitations may prevent loading on older iPads.

## Video generation
The video panel requires an authorized HTTPS GPU endpoint. POST JSON `{"prompt":"..."}`; respond with JSON `{"video_url":"https://...mp4"}` or a video response. CORS must permit the app's origin. No free GPU or video backend is included.

## Privacy
Chat history uses localStorage. The bearer token is not persisted. Never commit secrets.
