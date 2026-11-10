# My Library

## One-time setup
1. Create a GitHub repo and upload everything in this folder.
2. Settings > Pages > Deploy from branch > `main` / root. Your site is then at `https://USERNAME.github.io/REPO/`.
3. Settings > Actions > General > Workflow permissions > Read and write (only needed if you also add books by hand).
4. Create a token: github.com/settings/personal-access-tokens > Fine-grained token.
   Repository access: only this repo. Permissions: Contents = Read and write.
5. Open your site, click "Owner settings", enter your username, repo name and the token, Save.
   The "+ Add book" button now appears on that browser.

## Adding a book
Click "+ Add book", pick the PDF and the cover image, fill in title, author, genre and year, then Upload.
The PDF, cover and the book list go into the repo in one commit. You can read the book straight away on the device you uploaded from. Other devices see it after GitHub Pages redeploys (about a minute).
If you leave the cover empty, the first page of the PDF is used.

## Removing a book
With the token set, each card has an ✕ button. It deletes the PDF and cover from the repo.

## Notes
- The token stays in that browser only. Other visitors can read but cannot add or remove. Don't save the token on a shared computer. Remove it with "Remove token".
- PDFs over 90 MB are refused (GitHub's file limit is 100 MB).
- You can still add books by hand: put `name.pdf` and `name.jpg` in `books/` and commit. The GitHub Action adds them to `books.json` and keeps the details you entered through the site.
- Site title: change `CFG.title` in `index.html`.
- Progress, favourites and theme are saved per visitor in their browser.
- To test locally, run `python -m http.server` in this folder.
