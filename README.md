# FRAME / LAB — Experiment 12
Khushi Jain Daga | 23bcon1665 | B.Tech CSE VII | JECRC University | Web Development Using AI | Mr Mohit Parashar | 2026–27

An original photography-inspired visual research laboratory. Imagine generates images through Gemini; Decode sends an uploaded image to Gemini for captions, alt text, composition and keywords. Session contact sheet supports revisiting outputs, image export and copying analysis. No database or dependencies required. Node 22.9+ recommended; Node 24 supported.

## Run
Copy `.env.example` to `.env`, enter Gemini API key and supported model names, then `npm start`. Open http://localhost:8011. `npm test` runs validation and HTTP smoke tests. Never commit `.env`. Live calls may incur charges; check provider access. Local preview is not AI output. Uploaded images are transmitted to Google only on submission. Do not upload confidential images. Session archive is memory-only and clears on refresh.

## Architecture
Browser → POST /api/studio → input validation → Gemini generateContent → image/text response → viewfinder and contact sheet. API key stays server-side. Server binds to loopback for academic use only. Not hardened for public deployment. GET /api/health checks key presence, not provider connectivity.

## Manual practical
Generate a desert observatory image with 3:2 ratio, export image, upload it in Decode, request caption and alt text, select previous frame. Capture actual output screenshots. Live provider results must be tested by student; no fabricated evidence.

## References
https://ai.google.dev/gemini-api/docs/image-generation
https://ai.google.dev/gemini-api/docs/image-understanding
