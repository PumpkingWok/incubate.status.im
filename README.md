# Status Incubate

This repo hosts the code for both [incubate.status.im](https://incubate.status.im) on the `master` branch (which builds and serves through `gh-pages`), and [dev-incubate.status.im](https://dev-docs.status.im) on the `develop` branch.

There is an `edit` button on each page, which will take you directly to the document you need to edit on the `develop` branch. We can then allow a large group of people to push directly to `develop` and show their changes on the staging site when asking for review, which should smooth out and speed up the process considerably for everyone. `master` is obviously protected, and will only have changes merged in from `develop` once accepted.

## Adding a New Page

If you want to add a page, rather than just edit, you'll need to make sure it appears on the sidebar and is accessible to everyone.

1. Add your page to `source/docs/<your_file_here>.md`
2. In `source/_data/sidebars.yml` add the appropriate text to the appropriate place.
3. In `themes/navy/languages/en.yml` edit the sidebars section to make sure that your new text in `sidebars.yml` is rendered correctly.

## Testing locally

Make sure you have node.js installed first.

1. Open Terminal and navigate to the project root directory,
2. Run `npm install`,
3. Run `npm run build`,
4. Go to `public/` directory,
5. Start a simple HTTP server serving files, for example: `python -m SimpleHTTPServer 8000`,
6. Open http://localhost:8000 in a browser.
