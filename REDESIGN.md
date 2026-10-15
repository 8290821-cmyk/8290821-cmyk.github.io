# Figma preview — 15 October 2026

This branch implements Page 2 of the supplied Figma file using the existing Hugo site. The live website has not been deployed or changed.

## Preview

Run the existing `pnpm dev` script with Hugo 0.156.0, Go, and Node available. For the preview prepared in this workspace, open http://127.0.0.1:4173/ while the local server is running.

The homepage, five research pages, Tiny Alchemists page, and four existing project pages use the new layout. Other legacy pages remain available. The homepage uses the supplied monochrome portrait with the latest Figma frame and icons. Tiny Alchemists includes the supplied artwork, a description based on the project website, and links to the project website and trailer. Published papers include CNKI and PDF links. The site icon uses the user-supplied logo.

## Edit

- `data/academic.json`: paper titles, statuses, summaries, detail sections and existing PDF links.
- `layouts/academic/`: home, research, and project templates.
- `layouts/_partials/academic/`: shared document head and publication card.
- `static/academic/`: responsive CSS and navigation enhancement.
- `static/figma/`: downloaded source design assets, served locally.
- `static/uploads/yufan-huang-cv.pdf`: the newly supplied CV. The old `resume.pdf` is preserved.
- Existing project Markdown, images, reports and publication pages are retained.

The original HugoBlox Inter font is reused. No framework or new production dependency was added. The existing GitHub Pages deployment workflow is unchanged.

## Recover the original

Original commit: `e8ea3ae29936203acc53d8064fb211b5b3e358f4`

Original local tag: `backup/pre-figma-2026-10-15`

Development branch: `codex/figma-preview`

Two independent backups are stored beside this repository in `../website-backups/`:

- `academic-website-original-2026-10-15.bundle` contains all fetched Git history and refs. Verified with `git bundle verify`.
- `academic-website-original-2026-10-15.zip` contains the original tracked source files.

To inspect or run the original without touching this branch, create a separate checkout:

```sh
git worktree add --detach ../academic-website-original backup/pre-figma-2026-10-15
```

If this checkout is lost, recover from the bundle into a new directory:

```sh
git clone ../website-backups/academic-website-original-2026-10-15.bundle ../academic-website-restored
git -C ../academic-website-restored switch main
```

No force push or reset is needed. If the redesign is deployed later, reverting its commit(s) and redeploying restores the old version while keeping history.

## Validation

Hugo builds the complete site. Browser QA covers homepage and research/project layouts at mobile, tablet, and desktop widths, all homepage page links, PDF/CV responses, image loading, and detail-page return navigation. Preview screenshots and the browser report are saved in `../website-preview/`.
