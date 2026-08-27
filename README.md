# Operation Fly, Fight, Win

Air Force PFRA preparation block. Two static pages, no build step, no dependencies.

    index.html     Training programme. 28 weeks, both athletes, with a log.
    kitchen.html   Nutrition plan.
    .nojekyll      Tells GitHub Pages to serve the files as-is.

## Putting it on GitHub Pages

1. Create a repository. Public if you want a public URL, private if you have
   a paid plan and want it restricted.
2. Upload all three files to the root of the `main` branch. Keep the names.
   Do not put them in a subfolder unless you also set the folder in step 3.
3. Settings, then Pages. Source: "Deploy from a branch". Branch: `main`,
   folder: `/ (root)`. Save.
4. Wait a minute. The URL appears at the top of that same Pages settings page,
   in the form `https://<username>.github.io/<repo>/`.

`index.html` is what loads at that address. `kitchen.html` sits at
`https://<username>.github.io/<repo>/kitchen.html` and the two link to each
other through the bar at the top, so nothing needs editing.

## Anywhere else

The same three files work unchanged on Netlify, Cloudflare Pages, Vercel, an
S3 bucket with static hosting on, or any web host with an FTP login. Drag the
folder in. They also open straight off a hard drive or a USB stick by
double-clicking `index.html`, which is worth knowing if the gym has no signal.

## The log

The training page has a **Log** tab. Enter a time trial and every pace on the
card repaces to it. Enter a 3 rep max at a block start and every working load
for those eight weeks calculates and shows up on the day card in pounds. There
is a profile switch at the top so one page serves both of you without the
entries colliding, and Hannah's symptom log only appears on her profile.

It computes and it flags. It does not rewrite the programme. Two rules fire on
their own: three sessions running at rung 2 or higher says referral, and a
consistent direction of relief in the symptom log gets named for what it
suggests.

**The log lives in the browser it was entered in.** It does not travel with the
link. Opening the site on another phone gives you the programme, not the log.
Three things cover that:

- **Export backup file** downloads the whole thing as JSON. Do it after any
  test week.
- **Import backup** reads that file back on any device.
- **Copy setup link** produces a short URL carrying the current VDOTs and
  working maxes only, about 150 characters, short enough to text. It
  deliberately leaves out the symptom log.

Clearing site data in the browser erases the log. Export is the backup.

## Notes

- The only outbound request either page makes is to Google Fonts. If a network
  blocks it the pages still work, they just fall back to system fonts.
- Both pages follow the reader's light or dark setting automatically.
- The training page remembers which week and day you last had open, in that
  browser only. Nothing is sent anywhere.
- `noindex` is set on both pages, so search engines will not list them. Remove
  the robots meta tag from the head of each file if you ever want them found.
- These pages carry personal medical detail. Consider that before putting them
  on a public URL.
