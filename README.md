# Operation Blue Line

Air Force PFRA preparation block. Two static pages, no build step, no dependencies.

    index.html     Training programme. 28 weeks, both athletes, interactive.
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
