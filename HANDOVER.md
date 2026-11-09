# Handover: Dinner Party Trivia

Read this first in any new session; rewrite it at the end.

_Last updated: 8 Nov 2026_

## What's live
- https://vikingkompis.github.io/dinner-party-trivia/ (public repo, GitHub Pages). Keep this address until Erik decides to go commercial; then buy a short domain.
- **v3 (7 Nov):** the laptop opens the app, presses "Show on TV" and is AirPlayed or plugged into the TV. Everyone, host included, joins by QR code and answers on their own phone. The first phone to join hosts: level, topics, timer, Start; Back, Pause, Skip; Next and ✓/✗ corrections on the reveal; Play again or Change setup. If the host phone drops for 12 s, the host role passes on.
- Question pool drawn per game; English and Swedish; Sverige 80-90 nostalgia level; answers shuffled each game. `terms.html` and `privacy.html` exist.

## How it's built
- One `index.html` plus `sw.js` and `manifest.webmanifest`. Bump the service worker version on every deploy.
- Phones connect to the TV screen through **PeerJS** using the free public server (0.peerjs.com). There is no TURN relay, so phones on mobile data may fail to join.

## Decisions (Erik)
- Everyone plays on a phone via QR; no pen and paper. The host must be able to play from the same phone, with all question types.
- Must scale; no Apple TV app.
- Played with friends and it went down very well; treat it as an MVP to expand and maybe commercialise.

## Not yet proven
- v3 has only been tested with simulated phones, not real ones over the public server. Erik's 2-minute test: laptop + two phones on home Wi-Fi.

## Next steps
1. Erik's real-phone test; fix what breaks.
2. Before any commercial step: move the connection from PeerJS to Supabase Realtime (Erik already uses Supabase), which fixes mobile data.
3. Grow the question catalogue (more topics and general knowledge).
4. Commercial basics: name check, domain, pricing idea.

## Keep it cheap
Skip simulated multi-phone testing and voiceover re-recording unless Erik asks; he tests on real phones.
