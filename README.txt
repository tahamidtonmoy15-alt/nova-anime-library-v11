NOVA — Premium Anime Library

SETUP
1. Extract this ZIP.
2. For offline PWA installation, publish the folder to an HTTPS static host.
3. Open the HTTPS address in Chrome and choose Install app / Add to Home screen.

USAGE
- Home: cinematic landing page and your anime collection.
- Watching: add a title, open Manage Episodes, and add a video to an episode.
- Tap the episode status to toggle Watched / Not Watched.
- Play Video opens the saved copy; Delete removes that episode's saved copy.
- More: Storage estimate, JSON export and import.

LIMITATIONS
Browser storage is quota-limited and may be cleared by browser/device settings. JSON backups do not include video blobs. Android Chrome works best with MP4 (H.264 video + AAC audio). Unsupported codecs may show sound without a picture. A browser player cannot guarantee support for every VLC codec or advanced audio-track feature.

MOBILE UPDATE: The Home hero now uses the second supplied reference image. The previous moon/silhouette SVG hero has been removed. The hero artwork is bundled locally and included in the offline cache.


NOVA v11 — External Android player handoff
- Tapping Play Video first asks Android to share the saved video file with a compatible installed app.
- Choose VLC, MX Player, or another app shown by Android. Returning from that player returns to NOVA.
- The video remains stored in NOVA's IndexedDB vault; deleting the original from Gallery does not delete NOVA's saved copy.
- This uses Android's system Sharesheet. A web/PWA app cannot enumerate installed apps or force VLC/MX Player to appear; availability depends on Android, Chrome, app version and file type.
- If the browser cannot share the file, NOVA falls back to its built-in browser player and retains Save to phone / external share controls.
- Browser storage can still be removed by clearing site data or uninstalling/resetting the browser; keep backups of important videos.
