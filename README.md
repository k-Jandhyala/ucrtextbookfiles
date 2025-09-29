# Files Static Site

A simple static site for hosting course materials and documents. Works on both GitHub Pages and Vercel.

## Deployment Options

### Option 1: GitHub Pages
1. **Enable GitHub Pages:**
   - Go to your repository settings
   - Navigate to "Pages" in the left sidebar
   - Under "Source", select "GitHub Actions"
   - The site will be available at: `https://[your-username].github.io/files.github.io/`

2. **Deployment:**
   - The site automatically deploys when you push to the `main` branch
   - The GitHub Actions workflow handles the deployment process

### Option 2: Vercel (Recommended)
1. **Deploy to Vercel:**
   - Connect your GitHub repository to Vercel
   - Vercel will automatically detect it as a static site
   - The `vercel.json` configuration optimizes PDF serving
   - Your site will be available at: `https://[your-project-name].vercel.app/`

2. **Advantages of Vercel:**
   - Better PDF handling and CORS support
   - Faster global CDN
   - Automatic HTTPS
   - Better caching for static assets

3. **Adding Files:**
   - Place PDF files in the `files/` directory
   - Update the links in `index.html` accordingly
   - Use relative paths (not absolute paths starting with `/`)

## File Structure

```
/
├── index.html          # Main page
├── files/              # Course materials directory
│   └── Engineering_Design_Visualization.pdf
├── vercel.json         # Vercel configuration
└── .github/workflows/  # GitHub Actions for deployment
    └── deploy.yml
```

## Troubleshooting PDF Issues

If PDFs don't display properly in Chrome:
1. Ensure the file path is relative (not starting with `/`)
2. Check that the PDF file is not corrupted
3. Verify the file is accessible at the GitHub Pages URL
