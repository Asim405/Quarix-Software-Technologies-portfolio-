# QAURIX Software Technologies Portfolio

A responsive, single-page portfolio website for QAURIX Software Technologies. The site is built with HTML, Tailwind CSS via CDN, and vanilla JavaScript.

## Run locally

1. Install Python if it is not already installed.
2. Open PowerShell in the project folder.
3. Start a local web server:

   ```powershell
   python -m http.server 8000
   ```

4. Open [http://localhost:8000](http://localhost:8000) in your browser.
5. Press **Ctrl+C** in PowerShell to stop the server.

You can also open `qaurix_software_technologies_landing_page.html` directly, but a local server is recommended so relative assets behave as they will after deployment.

## Deploy with GitHub Pages

GitHub Pages is a good fit for this project because it is a static website and the repository is already hosted on GitHub. No server or build step is needed.

### 1. Prepare the homepage

GitHub Pages looks for an `index.html` file at the root of the published folder. Rename the current landing page to `index.html` before deployment. In PowerShell, run:

```powershell
Rename-Item .\qaurix_software_technologies_landing_page.html index.html
```

Keep `favicon.png`, `favicon.svg`, and the `docs` folder in the repository. The page uses relative paths to these files.

### 2. Save and push the change

From the project folder, run:

```powershell
git add -A -- README.md index.html qaurix_software_technologies_landing_page.html favicon.png favicon.svg docs
git commit -m "Prepare portfolio for GitHub Pages"
git push origin main
```

If you have not configured Git on this computer, follow GitHub's instructions to set up Git and authenticate first.

### 3. Enable GitHub Pages

1. Open the repository on GitHub: [Asim405/Quarix-Software-Technologies-portfolio-](https://github.com/Asim405/Quarix-Software-Technologies-portfolio-).
2. Select **Settings**.
3. In the sidebar, select **Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and the `/ (root)` folder, then select **Save**.
6. Wait for the Pages deployment to finish. The Pages settings screen will show the published website link.

The expected URL is:

```text
https://asim405.github.io/Quarix-Software-Technologies-portfolio-/
```

If GitHub shows a different link in **Settings → Pages**, use the link shown there.

### 4. Update the live site

After the first deployment, publish changes by committing and pushing them to `main`:

```powershell
git add .
git commit -m "Describe your website update"
git push origin main
```

GitHub Pages will redeploy the site automatically.

## Other static hosting options

You can also deploy the site using Netlify or Cloudflare Pages. Connect the GitHub repository in the hosting provider, select the `main` branch, leave the build command empty, and use the repository root as the publish directory. The homepage still needs to be named `index.html`.

## Important notes

- The **Add Client Proof** form stores entries in the current browser's local storage. Entries are not uploaded to a server and are not shared with other visitors. Shared testimonials require a backend or content-management service.
- The contact form submits to the Formspree endpoint configured in the HTML. Confirm that the endpoint belongs to your account and is active before publishing.
- Tailwind CSS, Google Fonts, and Font Awesome are loaded from external CDNs, so those assets require an internet connection.
