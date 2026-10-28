# VeteransUnderstand

Made by veterans, for veterans.

A free web tool for veterans living with PTSD, anxiety, and agoraphobia. It is insight-first: it helps you figure out what is happening and why, spot your own patterns earlier, and get through an episode with a little more control.

It does not promise a cure, a fix, or that symptoms will go away. It promises understanding — peer experience, written by a veteran, not a diagnosis or medical treatment.

> If you are in crisis or feel unsafe, call the Veterans Crisis Line: **988, then press 1**.

## What is on the site

The site is a single page. Everything on it is free to read and use — no account, no sign-up, no subscription, and no premium version.

- **Opening piece** — "Why It Doesn't Just Go Away — And Why Understanding Still Changes It"
- **Symptoms don't all look the same** — loud, quiet, and crash patterns, with a note to get new, severe, or worrying physical symptoms checked medically
- **In-the-moment tools** — for when an episode is already happening:
  - My episode plan — what calm-you wrote for episode-you, including a one-tap trusted contact
  - Breath timer
  - Safe-place scan
  - Body check
  - Leave-now script
  - Ride-it-out timer
- **After an episode — a quick debrief** — what set it off, what helped, and how long it lasted
- **Trace the pattern** — a pattern log, your early-warning signs, small levers, and a step ladder for going out
- **Stories from other veterans** — shared only with consent, anonymous or first name only
- **Resources beyond this page** — ongoing care, peer support, housing, benefits, and work, plus the Veterans Crisis Line
- **Privacy Policy** — a full section on the page, covering cookies, advertising, and what the page does and does not collect

## Privacy in one paragraph

On this public static version, anything you type — episode plan, pattern log entries, debriefs, early-warning signs, step ladder, or a story draft — stays in the memory of that visit, on your device. It is not sent to a server, not saved, not sold, and not used to choose ads for you. Leaving or refreshing the page clears it.

See the Privacy Policy section on the page itself for the full wording, including how Google AdSense and third-party advertising cookies work and how to opt out.

## Repository layout

```text
.
├── index.html   # The whole site — one self-contained static file
└── README.md    # This file
```

There is no build step, no framework, and no backend. Edit `index.html`, commit, and GitHub Pages serves the new version.

The exported source file for this site was named `veteran-support-tool-public.html`. In this repository it must be named `index.html` and sit at the root, because GitHub Pages serves `index.html` at the site root — and that root is what services such as Google AdSense check.

## GitHub Pages setup

This README is for the **user-site** repository:

- Repository: `leqwa010-pixel.github.io`
- Branch: `main`
- Folder: `/ (root)`
- Target address: https://leqwa010-pixel.github.io/

Setup, if Pages is not on yet:

1. Put the site file in the repository root and name it `index.html`.
2. Put this file in the repository root as `README.md`.
3. In the repository, go to **Settings > Pages**.
4. Under **Build and deployment**, set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
5. Wait for the Pages build to finish, then open the target address and check that the page loads with the tagline "Made by veterans, for veterans.", the Privacy Policy section, and the Veterans Crisis Line footer.

Status note: as of October 28, 2026, this address was not live yet — it returned GitHub Pages' "Site not found" 404 page. Do not submit it to AdSense until it actually loads the tool.

There is also a separate project repository named `Veteransunderstand`. Do not delete it. It is not the GitHub Pages / AdSense target — this user-site repository is.

## Working in Codespaces

1. Open the `leqwa010-pixel.github.io` repository on GitHub and choose **Code > Codespaces > Create codespace on main**.
2. Edit `index.html` directly. All content, styles, and scripts are in that one file.
3. Preview locally in the codespace terminal:

   ```bash
   python3 -m http.server 8000
   ```

   Then open the forwarded port 8000 in the browser preview.
4. Check the page at a phone width as well as desktop width before committing — most visitors will be on a phone.
5. Commit and push to `main`. GitHub Pages republishes automatically from that branch.

```bash
git add index.html README.md
git commit -m "Update veteran support tool"
git push origin main
```

## Advertising and AdSense

The tool stays free for veterans because it is supported by ads, not by charging veterans.

- The `<head>` of `index.html` contains a Google AdSense account Meta tag for site verification. Do not remove or change it — AdSense checks for it at the site root.
- AdSense can only verify a site at its root domain. That is why this tool is hosted on its own GitHub Pages user site instead of under a shared domain such as muse.ai, where AdSense only sees the shared root.
- Keep ads clearly labelled, placed between sections, and never inside a visitor's personal entries and never next to the Veterans Crisis Line.
- The page currently also carries a direct Iron Compass house ad and a reserved, clearly labelled ad slot. Keep any future ad in that same labelled slot style.

Do not add an `ads.txt` publisher entry, a new AdSense code snippet, or any other publisher code unless it is copied exactly from the AdSense account for this site.

## House rules for edits

- **Free, always.** No paywall, subscription, or locked "premium" help.
- **Insight, not a cure.** Do not rewrite copy to promise fixing or eliminating PTSD, anxiety, or agoraphobia.
- **No invented stories.** Veteran stories go on the page only when a real veteran shared theirs and chose anonymous or first-name credit.
- **Visit-only entries.** Do not add a server, account system, or analytics that receives a visitor's episode plan, log, debrief, signs, ladder, or story draft without updating the Privacy Policy first and getting the site owner's approval.
- **Crisis line stays prominent.** Keep "988, then press 1" visible in the in-the-moment section and in the footer.
- **Not medical advice.** Keep the peer-experience wording and the note to get worrying physical symptoms checked.

## Licence and reuse

No licence has been chosen for this repository yet, so the code and writing are all rights reserved by default. Ask the site owner before reusing the text or tools elsewhere.
