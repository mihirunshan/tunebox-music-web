# TuneBox Music Web

A personal-use, Spotify-inspired music interface built with HTML, CSS and JavaScript. It searches YouTube Data API v3 and plays videos through the official YouTube IFrame Player.

## Run it
1. Extract this folder.
2. Recommended: run a local static server in this folder (for example, VS Code Live Server) and open `index.html` through it. Direct `file://` may work in some browsers but local server is more reliable.
3. Click **Settings**, paste your YouTube Data API v3 key, and save.
4. Search for a song, artist or genre. Use **+** to add a result to the queue; click a quick pick to play it.
5. Queue controls, next/previous, shuffle, repeat, volume, seek, playlists and liked-track toggles are included.

## Enable the API
In Google Cloud Console, enable **YouTube Data API v3**, create an API key, and restrict it to YouTube Data API v3 where possible. If you use HTTP referrer restrictions, add your local development origin (for example `http://localhost:5500/*`) to the key's allowed referrers. Never publish your key or commit it into source code.

## Important limitations
- YouTube Data API is a search/metadata API; it does not give this app direct access to raw audio streams. Playback is through YouTube's embedded player and follows YouTube availability, ads, restrictions, and embed permissions.
- This is not Spotify Premium and cannot provide Spotify's proprietary catalog, offline downloads, Spotify-only features, or ad-free YouTube playback.
- YouTube API quotas and Google/YouTube terms apply. Some videos may refuse embedded playback.
- API key is stored in this browser's localStorage on this device. Clear it from Settings to remove it.
- Playlists and liked-track choices are saved locally in this browser only; no cloud sync.
