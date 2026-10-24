# Uktub Speak AI — starter project

A seven-language speaking-practice website starter (Arabic, English, German, French, Russian, Kyrgyz, Turkish). It includes a multilingual UI, browser speech recognition/speech synthesis where supported, and a server-side AI assessment route.

## Requirements
- Windows 10/11
- Node.js LTS installed
- An API key for the AI provider used by this starter

## Run locally (Windows)
1. Extract the ZIP into a folder, for example `Desktop\uktub-speak-ai`.
2. Install Node.js LTS from the official Node.js website if `node --version` does not work.
3. Open Command Prompt in the project folder.
4. Run `npm install`.
5. Copy `.env.example` to `.env.local`.
6. Open `.env.local` in Notepad and replace `replace_with_your_private_api_key` with your private API key. Keep this file private; never upload it to GitHub.
7. Run `npm run dev`.
8. Open `http://localhost:3000` in Chrome or Edge.
9. Allow microphone access when prompted.

## Deploy publicly
1. Create a private GitHub repository and upload the project files, but do NOT upload `.env.local`.
2. Import the repository into Vercel.
3. In Vercel project Settings → Environment Variables, add `OPENAI_API_KEY` and `OPENAI_MODEL` with the values you use locally.
4. Deploy and test the production URL. Microphone access requires HTTPS; Vercel provides HTTPS.
5. Do not share the API key in screenshots, chat, or source code.

## Important limitations of this starter
- This is a first working MVP, not yet a full official exam simulator.
- Browser speech recognition support and accuracy vary by browser, device, locale, and language. Kyrgyz speech recognition may be unavailable in a browser; typed answers remain available.
- The AI assesses the transcript, not actual pronunciation. A pronunciation score requires audio-aware evaluation.
- The app currently does not include accounts, persistent history, payments, abuse prevention, or per-user usage limits. Add these before opening it widely to the public, or someone could consume your API quota.
- API model availability and billing depend on your AI provider account. If the configured model is unavailable, set `OPENAI_MODEL` to a model available in your account.
- Do not present AI estimates as official CEFR certificates.
