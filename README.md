# John Martin™ Portfolio — Vercel deployment

The existing portfolio design and inquiry form fields are preserved. The inquiry form submits directly to Web3Forms using the provided form access key. Web3Forms delivers submissions to the recipient email configured for that access key.

## Deploy to Vercel

1. Upload the contents of this folder to your GitHub repository (the `index.html` file must be at the repository root).
2. Import the GitHub repository into Vercel and deploy with the default settings. No build command or environment variables are required for this static HTML site.
3. In Web3Forms, confirm that the access key is configured to deliver submissions to **champagnemrtn@gmail.com**. Complete any email verification requested by Web3Forms.
4. After deployment, submit a test inquiry from the live website and confirm it arrives in your inbox.

## Included changes

- Kept all existing inquiry form fields and project-type options exactly as they were.
- Replaced the Resend/Vercel API flow with a direct Web3Forms submission.
- Preserved the site's sending, success, and failure messages and visual styling.
- Sends the visitor's name, email, project type, optional budget, and project idea.
- Restored all four portfolio video clips under `public/videos/` and updated the video player paths to Vercel-compatible `/videos/...` URLs.
- Kept the right-click context-menu deterrent for images and videos, including dynamically created video elements.

## Access key note

Web3Forms access keys are intended to be used in website form code, so the key appears in the client-side HTML. You can restrict allowed domains in your Web3Forms settings if that option is available on your account. Do not put private account passwords or unrelated API secrets in this repository.

## Media protection limitation

Blocking the context menu only discourages casual right-click saving. It cannot prevent screenshots, screen recording, browser developer tools, cached media access, or other ways of copying content.


## Video files

The four MP4 files are included in `public/videos/`. Keep this folder in the GitHub repository; Vercel serves these files from `/videos/` after deployment.


### Favicon
The supplied white transparent logo is installed as the site favicon (`public/favicon.ico` and PNG sizes) and Apple touch icon. The HTML references these assets from the site root.
