# Our Arcade: setup

## One-time setup
1. Create a free Firebase project with a Firestore database and publish the rules in `firestore.rules`.
2. Open `config.js` and replace the four `PASTE_...` values with yours (Firebase > Project settings > Your apps).
3. Upload all files to your GitHub repository. Vercel updates the site automatically.

## Updating later
Only `index.html` changes when games change. Your Firebase values live in `config.js`, so you never have to paste them again. Just upload the new `index.html`.
