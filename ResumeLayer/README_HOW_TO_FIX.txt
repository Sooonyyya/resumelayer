ResumeLayer – GitHub Pages email confirmation fix

WHAT CHANGED
- The waitlist now shows: "Your email has been added to the waitlist!" when the Google Apps Script response reaches the hidden iframe.
- Fixed the false negative caused by the Google Apps Script response being wrapped inside a separate iframe, so its postMessage may not reach the landing page.
- Kept the existing Google Apps Script URL, saved emails, landing design and static GitHub Pages support.

HOW TO DEPLOY
1. Unzip this archive.
2. Replace index.html in the root of your GitHub repository with this version.
3. Keep .nojekyll in the repository root.
4. Wait for the Pages deployment and hard-refresh (Ctrl+Shift+R).
5. Test with a NEW email and confirm the record appears in the Waitlist sheet.

NOTE
An iframe load is a fallback signal that the response loaded, not a cryptographic confirmation that a spreadsheet record was written. Check the Sheet for the first test. The original server-side success / duplicate responses are still handled if they arrive.
