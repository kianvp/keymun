# Keystone Model United Nations

The website for KeyMUN — Keystone School, Hyderabad.

Made by Kian Veer and Yashashwin Reddy, Grade 9A.

## Running it

There is no build step. `index.html` is the whole site — open it in a browser,
or serve the folder with any static server.

## Editing the content

Almost everything on the site is rendered from one object near the top of the
`<script type="module">` block in `index.html`, called `DATA`. Change it there
and the page follows.

| What | Where in `DATA` |
| --- | --- |
| Registration form link | `formUrl` |
| Scrolling announcements | `announcements` |
| Home page counters | `stats` |
| Committees (name, agenda, description) | `committees` |
| Secretariat & Executive Board | `people` |
| Organising Committee | `oc` |
| Gallery captions | `gallery` |
| Three-day programme | `schedule` |
| Guides and document links | `resources` |
| Frequently asked questions | `faq` |

The nine photos in the opening animation are listed separately in `MUN_PHOTOS`,
further down the same script. Local paths like `photos/mun1.jpg` work fine.

## Admin console

An unlisted page at `#/admin` (or press **Ctrl+Shift+K**) shows a checklist of
content that still needs filling in.

Note that this site is a single static file with no server, so the passphrase
gate is a soft one — anyone reading the page source can work it out. It keeps
the console out of the way; it is not security. Do not put anything private
behind it.

## Structure

Single file, no dependencies to install. It pulls three things from CDNs at
runtime: the Archivo Black and Inter typefaces, `anime.js` for animation, and
`page-flip` for the Secretariat book. If `page-flip` fails to load, the
Secretariat page falls back to a flat grid rather than rendering empty.
