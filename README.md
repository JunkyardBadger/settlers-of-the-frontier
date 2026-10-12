# Settlers of the Frontier

This folder is the website. Upload it to GitHub Pages, then connect Firebase so friends can share a table. A turn can wait a day. Trade offers still expire after 24 hours.

## 1. Firebase

1. Go to [Firebase console](https://console.firebase.google.com/) and create a project.
2. Add a **Web** app. Copy the config values.
3. Open `firebase-config.json` in this folder and paste them in. Leave no empty `projectId`, `apiKey`, or `appId`.
4. In Firebase, create a **Firestore Database**.
5. Open the Firestore **Rules** tab and paste the contents of `firestore.rules`, then publish.

The room code is the only password. Do not turn the rules to fully public beyond that file.

## 2. GitHub Pages

1. Create a public repository, for example `settlers-of-the-frontier`.
2. Upload **every file in this folder** to the root of the repository.
3. **Settings → Pages → Deploy from a branch**.
4. Branch `main`, folder `/ (root)`. Save.
5. Open the site GitHub shows, usually `https://YOUR-NAME.github.io/settlers-of-the-frontier/`.

If you change `firebase-config.json` later, upload that file again. Reload the site.

## How a table works

- **Host** enters a name and creates a room. Share the 4-letter code.
- **Join** is for friends. Each person enters their own name.
- The host picks the map, the points, and starts.
- The game is stored in Firebase. Close the phone and come back with **Rejoin** on the same device.
- Whoever's turn it is can play, even if the host is away.
- An unanswered trade is rejected automatically after 24 hours.

Solo and pass-and-play stay on the phone and do not use Firebase.
