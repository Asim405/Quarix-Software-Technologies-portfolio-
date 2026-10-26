# QAURIX Software Technologies Portfolio

A responsive, single-page portfolio website built with HTML, Tailwind CSS via CDN, and vanilla JavaScript. It is a static site: no build process or application server is required.

## Run locally

1. Open PowerShell in the project folder.
2. Start a local web server:

   ```powershell
   python -m http.server 8000
   ```

3. Visit [http://localhost:8000](http://localhost:8000).
4. Press **Ctrl+C** in PowerShell to stop the server.

## Deploy to Vercel

1. Push this project to a GitHub repository. The root of the repository must contain `index.html`, `favicon.png`, `favicon.svg`, and the `docs` folder.
2. Sign in to [Vercel](https://vercel.com/) and choose **Add New... → Project**.
3. Import the GitHub repository containing this site and authorize access if prompted.
4. In the project configuration:
   - Set **Framework Preset** to **Other**.
   - Leave **Build Command** empty.
   - Leave the output directory at the project root (`.`) or use `.` if Vercel requests a value.
   - Leave the install command empty.
5. Choose **Deploy**. When it finishes, open the deployment URL shown in the Vercel dashboard.

Vercel can redeploy the site automatically whenever you push changes to the connected branch.

## Deploy to Netlify

### Connect the GitHub repository

1. Sign in to [Netlify](https://www.netlify.com/) and choose **Add new project → Import an existing project**.
2. Choose GitHub, authorize access if prompted, and select the repository containing this site.
3. Set the build settings:
   - **Base directory**: leave blank.
   - **Build command**: leave blank.
   - **Publish directory**: `.` (the repository root).
4. Choose **Deploy** and open the site URL shown in Netlify.

Netlify can redeploy automatically whenever you push changes to the connected branch.

### Manual Netlify deploy

You can also use Netlify's manual deploy/drop feature. Upload the project folder's site files, including `index.html`, `favicon.png`, `favicon.svg`, and `docs`. Do not upload just the HTML file; the page needs its neighboring assets.

## Update the deployed website

Edit the site locally, then commit and push the changes to the branch connected to Vercel or Netlify. For example:

```powershell
git add README.md index.html favicon.png favicon.svg docs
git commit -m "Update portfolio website"
git push
```

The hosting provider will build and publish the update automatically. There is no build command for this project.

## Other hosting options

This static site can also be hosted on GitHub Pages, Cloudflare Pages, or a standard web host. For a standard web host, upload the project files to its public web directory (often named `public_html` or `www`). Ensure `index.html` is in the published root directory.

## Important notes

- The **Add Client Proof** form stores entries in the current browser's local storage. Entries are not uploaded to a server or shared with other visitors. Shared testimonials require a backend or content-management service.
- The contact form submits to the Formspree endpoint configured in `index.html`. Confirm that the endpoint belongs to your account and is active before publishing.
- Tailwind CSS, Google Fonts, and Font Awesome are loaded from external CDNs, so those assets require an internet connection.
