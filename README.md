# CardBaazi site

Public pages for CardBaazi (privacy, support, and private-table invites).

Live: [https://ra2630.github.io/cardbaazi-site/](https://ra2630.github.io/cardbaazi-site/)

## Private-table invites

WhatsApp and other chats need a tappable **https** link. Share:

`https://ra2630.github.io/cardbaazi-site/join.html?code=ROOM&game=GAME`

That page tries to open the app with `cardbaazi://join?code=&game=` (bundle `com.soltech.CardGameApp`, team `M447KXNFDS`) and shows the room code so it can be typed if the app does not open.

`/join/` and `/join/CODE` also resolve to this flow (via `join/index.html` and `404.html`).

## Universal Links

Do **not** add `apple-app-site-association` on this GitHub Pages project site. Apple fetches AASA only from the host apex (`https://<host>/.well-known/apple-app-site-association`). A file under `/cardbaazi-site/` is ignored, so `*.github.io` project pages cannot serve Universal Links.

Add Associated Domains / AASA after a **custom domain** points at this site. `.nojekyll` is in the repo so a future `.well-known` directory is not skipped by Jekyll.
