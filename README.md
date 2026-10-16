# Checkmate Chess Club — Wood Edition

A responsive front-end prototype for a modern online chess club, using warm wood-brown and ivory styling. The chessboard uses an 8×8 grid with equal-sized squares, ivory/light squares, wood-brown/dark squares, and contrasting white and dark chess-piece glyphs with layered shadows.

## Files

- `index.html` — page structure and sample club content
- `css/styles.css` — responsive layout, wood palette, board and piece styling
- `js/app.js` — demo interactions for board selection/moves, navigation, sample lessons, tournament buttons, and local chat
- `config.example.js` — safe placeholder for future Supabase configuration

## Run locally

**Option A: VS Code Live Server**
1. Extract the ZIP file.
2. Open the extracted `checkmate_chess_club_wood` folder in VS Code.
3. Install the VS Code extension **Live Server** if needed.
4. Right-click `index.html` and choose **Open with Live Server**.

**Option B: Python**
From this folder, run `python -m http.server 8000`, then visit `http://localhost:8000`.

## Publish with Firebase Hosting

1. Open the folder in VS Code and make sure Firebase CLI is logged in.
2. In `firebase.json`, set Hosting's `public` directory to `.` and preserve any other settings you need. Example:

```json
{
  "hosting": {
    "public": ".",
    "ignore": ["firebase.json", "**/.*", "**/node_modules/**"]
  }
}
```

3. Run `firebase deploy --only hosting`.
4. Open the Hosting URL shown in the terminal.

Do not publish private files, service-role keys, `.env` files, or credentials. The ignore rules above exclude hidden files and `node_modules`, but review the folder before deployment.

## Supabase integration status

This is a front-end demo. Sample profiles, ratings, tournaments, and lesson content are illustrative. The chat only adds messages to the current page; it is not a shared live chat. The board allows basic piece selection and demo movement but **does not implement full legal chess rules, check/checkmate, castling, en passant, or robust bot strategy**. Real accounts, persistent profiles, rated games, secure multiplayer, tournament registration, and live chat must be integrated with Supabase and tested.

If you connect Supabase, use only the project's URL and publishable/anon key in browser code, with Row Level Security policies correctly configured. Never put a Supabase service-role or secret key in public frontend files.

## Customize

Edit colors near the top of `css/styles.css`. Board squares are controlled by `.sq.light` and `.sq.dark`; the board is explicitly an 8-column by 8-row grid, and the board container is square (`aspect-ratio: 1/1`) so each square stays equal-sized.
