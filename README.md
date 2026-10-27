# Divya Makkenchery — Personal Portfolio

A responsive, standalone HTML/CSS/JavaScript portfolio designed for recruiters and hiring managers. It can be previewed locally and published with GitHub Pages. It does not require Node.js, npm, a framework, or a build step.

## Files

- `index.html` — page content and project details
- `styles.css` — layout, responsive design, colors, typography
- `script.js` — mobile navigation and helpful placeholder-link alerts
- `assets/` — add your portrait and resume here

## 1. Personalize before publishing

### Add your photo
1. Choose a professional headshot.
2. Copy it into the `assets` folder and name it `divya-photo.jpg`.
3. If your image uses another format/name, change the image path in `index.html` at `assets/divya-photo.jpg`.

The site includes a placeholder design that appears if the photo file is missing.

### Add your resume
1. Export your resume as a PDF.
2. Put it in `assets/` named `Divya-Makkenchery-Resume.pdf`.
3. In `index.html`, find the Resume section and change the link from `href="#"` to `href="assets/Divya-Makkenchery-Resume.pdf"`.

### Add project repository links
In `index.html`, search for `data-placeholder="Add your repository URL"`. Replace each `href="#"` with the real URL for that project. If a project is not public, you can instead link to a short project write-up or remove the link.

### Review all content
Before publishing, confirm the education, experience, and skill wording is accurate. Replace the RAG course-project summary with the specific project goal and tools you used. Add project results only when you can verify them. Remove any placeholder notes you do not want visitors to see (search for `placeholder-reminder` and `Section-footnote`).

### Update links
GitHub and LinkedIn are currently set to:
- https://github.com/divyamakk
- https://www.linkedin.com/in/divyamakkenchery/
Email: `makkdivya@gmail.com`

## 2. Preview locally

**Simplest method (no terminal required):**
1. Open the portfolio folder in VS Code.
2. Install the VS Code extension **Live Server** if you do not already have it.
3. Right-click `index.html` in the Explorer.
4. Select **Open with Live Server**.

You can also double-click `index.html` to open it in a browser. Live Server is preferable while editing because it refreshes the page when you save changes.

## 3. Publish with GitHub Pages

### Recommended: create a separate repository first
This keeps your current Gitfolio project intact until the new site is ready.

1. In GitHub, create a **new public repository** named `divyamakk.github.io` (assuming `divyamakk` is your GitHub username).
2. Do not select a README, license, or `.gitignore` when creating it if you plan to push this folder as-is.
3. In VS Code, open the new portfolio folder (`divya-portfolio`), not the old `gitfolio` folder.
4. Open **Terminal → New Terminal** in VS Code.
5. Run these commands from inside the `divya-portfolio` folder:

   ```bash
   git init
   git add index.html styles.css script.js README.md assets
   git commit -m "Create personal portfolio website"
   git branch -M main
   git remote add origin https://github.com/divyamakk/divyamakk.github.io.git
   git push -u origin main
   ```

6. In the new GitHub repository, open **Settings → Pages**.
7. Under **Build and deployment**, choose **Deploy from a branch**.
8. Select branch `main` and folder `/(root)`, then save.
9. Wait for GitHub Pages to publish. Your site should be available at `https://divyamakk.github.io/`. It may take several minutes for the first deployment.

If GitHub says the remote already exists, run `git remote -v` to inspect it before changing anything. Do not overwrite a repository you care about.

## 4. Safely replace your current Gitfolio project

**Do not delete your current `gitfolio` folder or overwrite your existing GitHub repository yet.** First publish this as a separate repository and check it on desktop and mobile.

Once the new site looks correct:
- Keep the old `gitfolio` folder as a backup until you are certain you no longer need it.
- If you want to replace an existing GitHub Pages site rather than use `divyamakk.github.io`, first check which repository currently publishes it: GitHub → repository → Settings → Pages.
- Back up the current repository before replacing files.
- Copy the new `index.html`, `styles.css`, `script.js`, and `assets/` into the publishing repository. Do not copy `node_modules`, `dist`, or the Gitfolio source files.
- Commit and push the changes. Check **Settings → Pages** to confirm the correct branch/folder is still selected.

## 5. Before sharing with recruiters

- [ ] Replace the portrait placeholder with your photo.
- [ ] Link your PDF resume.
- [ ] Replace or remove all repository placeholders.
- [ ] Remove all bracketed editing notes and verify the project descriptions.
- [ ] Check email, GitHub, and LinkedIn links.
- [ ] Test the site on a phone and desktop.
- [ ] Open the published URL in a private/incognito window to confirm it is public.

## Notes

- The page uses Google Fonts loaded from the web. If offline, fallback fonts will be used.
- No analytics or tracking scripts are included.
- GitHub Pages serves static files; this site needs no server-side code.
