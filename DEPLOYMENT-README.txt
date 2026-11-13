# 786 CNC Workshop website - deployment guide

This is your existing HTML/CSS/JavaScript website prepared for free static hosting.

## What was changed
- Kept your existing design, service sections, images, navigation and WhatsApp links.
- Updated the contact form so it can send enquiries to your email through Web3Forms.
- Added an optional customer email field, submission status messages and a WhatsApp fallback.
- The email form is intentionally not active until you add your own Web3Forms access key.

## Before publishing: activate email enquiries
1. Go to https://web3forms.com/
2. Enter the email address where you want to receive customer enquiries.
3. Create an access key and complete the email verification step.
4. Open `index.html`.
5. Find `ADD_YOUR_WEB3FORMS_ACCESS_KEY_HERE`.
6. Replace it with your Web3Forms access key. Do not send the key to anyone.
7. Save and test the form using your own email/phone.

The Web3Forms access key is designed for browser-side form submissions. Do not put passwords, private API keys or other secret credentials in this website.

## Publish free with Cloudflare Pages + GitHub
1. Extract this ZIP file.
2. Create/sign in to a GitHub account: https://github.com/
3. Create a new **Public** repository, for example `786-cnc-workshop`.
4. Upload the contents of the `786-cnc-website` folder to the repository root. The root must contain `index.html` and the `assets` and `google photos` folders.
5. Open https://dash.cloudflare.com/ and create/sign in to a free account.
6. In Cloudflare, go to **Workers & Pages** -> **Create application** -> **Pages** -> **Connect to Git**.
7. Connect GitHub and select your repository.
8. For a plain HTML site, leave the build command empty. Set the build output directory to `/` (the repository root). If the interface asks for a root directory, use `/`.
9. Deploy. Cloudflare will provide a `*.pages.dev` address.
10. Open the live URL on both desktop and mobile. Test every navigation link, phone/WhatsApp buttons, images and the contact form.

## Important notes
- This is a static business website. It does not need a database, admin dashboard or Node.js server for the features currently requested.
- To change services, text or gallery images later, edit the website files and push the changes to GitHub. Cloudflare Pages will redeploy automatically.
- A custom domain is optional and usually costs money to register. The `pages.dev` address is free.
- Free service limits and terms can change. Check the current Cloudflare and Web3Forms plan pages before relying on them for high-volume use.
- Keep a copy of the original ZIP as a backup.
