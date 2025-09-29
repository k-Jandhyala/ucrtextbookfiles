# Files GitHub Pages Site

A simple static site for hosting course materials and documents.

## Setup Instructions

1. **Enable GitHub Pages:**
   - Go to your repository settings
   - Navigate to "Pages" in the left sidebar
   - Under "Source", select "GitHub Actions"
   - The site will be available at: `https://[your-username].github.io/files.github.io/`

2. **Deployment:**
   - The site automatically deploys when you push to the `main` branch
   - The GitHub Actions workflow handles the deployment process

3. **Adding Files:**
   - Place PDF files in the `public/` directory
   - Update the links in `index.html` accordingly
   - Use relative paths (not absolute paths starting with `/`)

## File Structure

```
/
├── index.html          # Main page
├── public/             # Public files directory
│   └── Textbooks/      # Course textbooks
│       └── Engineering_Design_Visualization.pdf
└── .github/workflows/  # GitHub Actions for deployment
    └── deploy.yml
```

## Troubleshooting PDF Issues

If PDFs don't display properly in Chrome:
1. Ensure the file path is relative (not starting with `/`)
2. Check that the PDF file is not corrupted
3. Verify the file is accessible at the GitHub Pages URL
