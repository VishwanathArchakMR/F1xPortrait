# Archak GP — F1-inspired portfolio

Static, frontend-only portfolio built for AWS S3 static website hosting.

## Run locally
Open `index.html` in a browser, or run a simple static server from this folder:
- Python: `python -m http.server 8000`
- Then visit `http://localhost:8000`

## Deploy to S3
1. Create an S3 bucket configured for static website hosting.
2. Upload `index.html`, `styles.css`, `script.js`, and the entire `assets/` folder.
3. Set `index.html` as the index document.
4. Configure public read access or use CloudFront + Origin Access Control for a production setup.
5. Add a custom domain later if desired.

## Notes before production
- This is a static frontend; no backend or API is required.
- The six project cards link to GitHub. NexusAct currently links to the profile because the exact repository slug was not supplied.
- Confirm the final public repository URL for IRIS and NexusAct, and replace any image assets if the uploaded screenshot filenames map differently.
- The portrait asset is the illustrated portrait supplied in the conversation.
- Fonts load from Google Fonts; for fully offline hosting, bundle font files locally.
- Racing-inspired sound effects use local assets only after a deliberate visitor action: `assets/drag-racing-2.mp3` for the opening start sequence, `assets/f1-racing.mp3` for project cards and non-link controls, and `assets/f1-radio.mp3` for every link. Each effect is a one-shot clip with a smooth fade-out; there is no continuous ambience and no third-party audio URL.
