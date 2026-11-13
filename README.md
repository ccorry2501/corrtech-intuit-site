# CorrTech Bookkeeping - Intuit App Pages

Static pages for the Intuit production checklist for the private CorrTech Bookkeeping app. Host these on GitHub Pages (free).

## Files
- index.html - App home / launch page
- privacy.html - Privacy Policy
- terms.html - Terms of Use (EULA)
- disconnect.html - Disconnect QuickBooks page
- callback.html - OAuth callback page (displays the code locally)

## GitHub Pages setup (about 10 minutes)
1. Create a new GitHub repository (public or private; GitHub Pages works with either).
2. Upload all 5 files to the repository root.
3. Go to Settings -> Pages. Under "Build and deployment", set Source to "Deploy from a branch", branch "main", folder "/ (root)". Save.
4. GitHub gives you a URL: https://<username>.github.io/<repo-name>/

## URLs to enter in Intuit (replace <your-url> with your GitHub Pages URL)
- Privacy Policy URL: <your-url>/privacy.html
- EULA URL: <your-url>/terms.html
- Host Domain: <username>.github.io
- Launch URL: <your-url>/index.html
- Disconnect URL: <your-url>/disconnect.html
- Production Redirect URI: <your-url>/callback.html

## OAuth callback flow
1. User clicks the Intuit sign-in link.
2. Intuit redirects to <your-url>/callback.html?code=...&realmId=...
3. The callback page reads the code from the URL and displays it on screen.
4. The user copies the code and pastes it into the Lindy conversation.
5. Lindy exchanges the code for tokens. The page itself makes no network calls and does not send the code anywhere; the code is part of the URL your browser loads, so it is transmitted to GitHub Pages as part of loading the page, as with any OAuth redirect.
