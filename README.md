# Our Arcade: setup (about 10 minutes, all free)

The game is one file (`index.html`). Rooms are stored in Firebase's free database. Vercel hosts the page.

## 1. Create the free Firebase database
1. Go to https://console.firebase.google.com and sign in with a Google account.
2. Click **Create a project**, name it anything (e.g. our-arcade), turn Google Analytics off, and create it.
3. In the left menu: **Build → Firestore Database → Create database**.
   - Choose any location close to you, and start in **production mode**.
4. Open the **Rules** tab, replace everything with the contents of `firestore.rules`, and click **Publish**.
5. Click the gear icon → **Project settings** → scroll to **Your apps** → click the **</>** (Web) icon.
   - Name it anything, skip hosting, and click **Register app**.
   - Copy the values from `firebaseConfig` (apiKey, authDomain, projectId, appId).

## 2. Paste the config
Open `index.html`, search for `PASTE_API_KEY`, and replace the four `PASTE_...` values with yours. Save.

## 3. Put it on Vercel
- Easiest: go to https://vercel.com/new, choose **Upload / drag and drop**, and drop this folder.
- Or with the CLI: run `npx vercel --prod` inside this folder.

Vercel gives you a link like `https://our-arcade.vercel.app`. Open it on both phones. The invite button in a room shares a link that fills in the room code automatically.

## Notes
- Your Firebase config is safe to be public in the page. The rules above let anyone with a room code play, which is fine for the two of you.
- Free tier limits are far above what two people will ever use.
