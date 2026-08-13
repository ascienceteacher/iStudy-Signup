RMA iStudy Hub — FIXED GitHub Version

WHAT CHANGED
- Removed the student and teacher "Class Teacher" dropdowns.
- Uses the actual Rowlie artwork from the prior RMA Mondrian design.
- Keeps 25 spaces PER SUBJECT.
- Student signup and teacher signup both write to the same Google Sheet.
- Teacher Hub tracks attendance, completion, no-shows, cancellations and notes.
- This version is designed for GitHub Pages + Google Apps Script API.

CRITICAL FIX FOR THE GOOGLE SHEET CONNECTION
Your current deployed Apps Script is still running an older doGet() that expects an Apps Script file named Index.html.

1. Google Sheet > Extensions > Apps Script
2. Open Code.gs.
3. Select all and replace it with the NEW Code.gs in this package.
4. Click Save.
5. DO NOT create Index.html in Apps Script.
6. Deploy > Manage deployments.
7. Click the pencil/edit icon on your existing web app.
8. Under Version choose NEW VERSION.
9. Deploy.
10. Open your /exec URL in a new browser tab.

It should now show JSON:
{"ok":true,"data":{"message":"iStudy API is running."}}

If you still see "No HTML file named Index was found", the old deployment is still active.

TEACHER ACCESS CODE
If your Settings tab does not already have:
Teacher Access Code | CHANGE-ME
add it in columns F/G, or run setupIStudySheet() once after replacing Code.gs.
Then replace CHANGE-ME with your staff code.

GITHUB
Upload BOTH:
- index.html
- rowlie.png

They must be at the same level in the repository root.

Do not upload Code.gs to GitHub; that stays in Apps Script.
