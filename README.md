# Abhishek Sharma Portfolio Website

Static personal portfolio website built from resume details. It is ready to upload to an S3 bucket and serve through CloudFront.

## Files

- `index.html` - portfolio content and page structure
- `styles.css` - responsive visual design
- `script.js` - mobile navigation and footer year
- `assets/abhishek-sharma.jpg` - profile image
- `assets/abhishek-sharma-resume.pdf` - downloadable resume

## Run Locally

Open `index.html` directly in a browser.

## Deploy To S3

From this folder:

```bash
aws s3 sync . s3://YOUR_BUCKET_NAME --delete
aws cloudfront create-invalidation --distribution-id YOUR_DISTRIBUTION_ID --paths "/*"
```
