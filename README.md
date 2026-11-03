# aquab1t.github.io

Personal portfolio of José Manuel Echevarría Rubio, PhD. One static page (`index.html`). The CV is not published on the site.

## Files

- `index.html`: the whole page (HTML and CSS inline; no scripts). Generated: do not edit by hand.
- `assets/currents.webp`: header background, surface current speed (turbo palette) in the open central Caribbean Sea (12.7 to 17.6° N, 63 to 71° W, no land) on 15 June 2025, daily mean of Copernicus Marine SMOC. Made from `OLCI_detection_and_tracking/data/forcing/events/eastern_caribbean_2025/smoc.nc`; the credit line is in the footer.
- `assets/jose_field.jpg`: portrait, resized to 900 x 900 px from `jose_pogo.jpg`.
- `.nojekyll`: tells GitHub Pages to serve the files as they are.

## Publish on GitHub Pages

1. On GitHub, create a **public** repository named exactly `aquab1t.github.io`.
2. From this folder:

   ```bash
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin git@github.com:aquab1t/aquab1t.github.io.git
   git push -u origin main
   ```

3. In the repository, open **Settings > Pages** and check that the source is "Deploy from a branch", branch `main`, folder `/ (root)`.
4. After a minute or two the site is live at https://aquab1t.github.io/.

## Edit the text

All the text on the page lives in `/media/jose/Work/sept/PostDocs/PORTFOLIO_CONTENT.md` (instructions at the top of that file). After editing it:

```bash
cd /media/jose/Work/sept/PostDocs
python3 MASTER/build_portfolio.py
```

The layout (CSS) is in `PostDocs/MASTER/portfolio_template.html`. Then publish the change:

```bash
cd /media/jose/Work/sept/aquab1t.github.io
git add -A && git commit -m "Update content" && git push
```

GitHub Pages redeploys in about a minute.

## Content rules

The figures on the page come from the verified facts file `PostDocs/POSTDOC_APPLICATIONS_CONTEXT_RESUME.md` and the manuscripts. Update the page when a paper's status changes (for example, the JMSE paper moving from "Submitted" to published, or the OLCI papers being submitted). Only link repositories that are public: `sargassum-olci-detection` and `sargassum-olci-drift` are private for now.
