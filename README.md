# The Don Jewelers & Jewelry

Vercel-ready static jewelry website with a serverless Labgrown Diamond inventory proxy.

## Deploy on Vercel

1. Upload or push this project to GitHub.
2. Import the repository into Vercel.
3. Add these Vercel environment variables:
   - `LABGROWN_DIAMOND_API_KEY`
   - `LABGROWN_DIAMOND_API_URL` set to `https://lgdusallc.com/developer-api/diamond`
   - `DIAMOND_CACHE_TTL_MS` set to `900000`
4. Use the default Vercel build settings. The build command is `npm run build`.

## Notes

- Do not commit a real `.env` file or private API key.
- Static files are served from `index.html`, `src/`, and `assets/`.
- The live diamond feed is served through `/api/diamonds` so the private vendor API key stays server-side.
- Checkout uses the configured Stripe Buy Button/payment link in `src/main.js`.
