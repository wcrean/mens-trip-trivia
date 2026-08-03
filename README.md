# Men’s Trip Trivia — Phase 1B

A simple phone-first multiplayer trivia proof of concept for the San Francisco Men’s Trip 2026. It runs directly on GitHub Pages and reuses the proven Firebase room, player, answer, and scoreboard flow from Search Party.

## Complete release files

- `index.html`
- `styles.css`
- `app.js`
- `firebase-service.js`
- `firebase-config.js`
- `questions.js`
- `firestore.rules`
- `README.md`

The existing Firebase web configuration remains included in `firebase-config.js`.

## Phase 1B scope

- Renamed as Men’s Trip Trivia
- Five temporary multiple-choice questions
- Five-round games only
- Existing create-room and join-room flow
- Host-controlled start, reveal, and next-round flow
- One point for each correct answer
- Final scoreboard
- Reveal button immediately disables after use to reduce duplicate-scoring risk

No categories, timers, free-text answers, host transfer, architecture changes, or main-app integration are included.

## Deploy

Replace all files in the repository root with the contents of this release. The repository root should directly show all eight files listed above.

## Firebase Authentication

In Firebase Console:

**Build → Authentication → Sign-in method → Anonymous → Enabled**

## Firestore rules

In Firebase Console:

**Build → Firestore Database → Rules**

Replace the editor contents with `firestore.rules`, then click **Publish**.

## GitHub Pages

In GitHub:

**Settings → Pages → Deploy from a branch → main → /(root) → Save**

After deployment, hard-refresh with **Ctrl+Shift+R** or use an incognito window.

## Phase 1B test

1. On Phone 1, create a five-round room.
2. On Phone 2, join using the room code.
3. Confirm both players appear.
4. Start the game.
5. Submit answers from both phones.
6. Reveal the correct answer.
7. Confirm each correct player receives exactly one point.
8. Advance through all five questions.
9. Confirm the final rankings are correct.

For this proof of concept, create a new room for each game rather than using **Play Again**.

## Question data

The five included questions are temporary test content. The downloadable question-bank workbook will become the source for later question updates.

## Suggested commit comment

> Convert Search Party into Men’s Trip Trivia Phase 1B proof of concept
