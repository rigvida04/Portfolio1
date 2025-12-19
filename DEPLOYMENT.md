# GitHub Pages Deployment Instructions

## Automatic Deployment (Recommended)

The repository is already configured with a GitHub Actions workflow for automatic deployment. To enable it:

1. **Enable GitHub Pages**:
   - Go to your repository on GitHub: https://github.com/rigvida04/Portfolio1
   - Click on **Settings** tab
   - Scroll down to **Pages** in the left sidebar
   - Under "Build and deployment":
     - Source: Select **GitHub Actions**
   - Save the changes

2. **Merge the Pull Request**:
   - Merge the current PR (#1) to the `main` branch
   - This will trigger the GitHub Actions workflow automatically

3. **Wait for Deployment**:
   - Go to the **Actions** tab to see the deployment progress
   - Once complete, your site will be live at: https://rigvida04.github.io/Portfolio1/

## Manual Setup (Alternative)

If you prefer to deploy without GitHub Actions:

1. Go to repository **Settings** > **Pages**
2. Under "Build and deployment":
   - Source: Select **Deploy from a branch**
   - Branch: Select **main** (or your default branch)
   - Folder: Select **/ (root)**
3. Click **Save**
4. Wait a few minutes for deployment
5. Your site will be available at: https://rigvida04.github.io/Portfolio1/

## Verifying Deployment

After deployment, test these features:

1. **Navigation**: Click on navigation links (Home, About, Projects, Contact)
2. **Smooth Scrolling**: Verify smooth scrolling between sections
3. **Contact Form**: Fill out and submit the contact form
4. **Responsive Design**: Test on different screen sizes
5. **Animations**: Check that sections fade in on scroll

## Troubleshooting

### Workflow shows "action_required"
- This means GitHub Pages is not yet enabled
- Follow Step 1 under "Automatic Deployment" above

### 404 Error
- Make sure `index.html` is in the root directory
- Check that the branch and folder are correctly configured in Settings > Pages

### Workflow fails
- Check the Actions tab for detailed logs
- Ensure GitHub Pages is configured to use "GitHub Actions" as the source

## Local Development

To test locally before deploying:

```bash
# Using Python
python3 -m http.server 8080

# Using Node.js
npx http-server -p 8080

# Using PHP
php -S localhost:8080
```

Then open http://localhost:8080 in your browser.

## Custom Domain (Optional)

To use a custom domain:

1. Go to Settings > Pages
2. Under "Custom domain", enter your domain
3. Follow GitHub's instructions to configure DNS
4. Enable "Enforce HTTPS" after DNS propagates

## Next Steps

After deployment:
- [ ] Update content in `index.html` with your information
- [ ] Add your actual projects to the Projects section
- [ ] Customize colors and styling in `styles.css`
- [ ] Add images and assets as needed
- [ ] Configure a custom domain (optional)
