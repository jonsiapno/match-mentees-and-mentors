# match-mentees-and-mentors

This Google Sheet automatically matches mentees with mentors from the same college. This README will guide you through using the spreadsheet, even if you have no technical background.

## What This Tool Does
This spreadsheet:

- Automatically pairs mentees with mentors from the same college
- Ensures each mentee gets exactly 1 mentor
- Ensures each mentor is assigned to no more than 1 mentee
- Creates a clean "Matches" sheet showing all the pairings

## Getting Started
### Step 1: Access the Template

1. Open the Google Sheet template I've shared with you
2. Make a copy for yourself by clicking File > Make a copy

![https://github.com/yourusername/your-repo/blob/main/screenshots/matches-tab.png](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20145900.jpg)

3. Give your copy a name (like "College Mentorship Matcher")

### Step 2: Add Your Participants

1. Go to the "Participants" sheet (tab at the bottom)
2. You'll see sample data already entered - replace this with your actual participant information:

- Full Name: The participant's name
- Email: The participant's email address
- Match Category: The college they're affiliated with
- Role: Either "Mentor" or "Mentee"

![https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20145900.jpg](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20150431.jpg)
Important: Don't change the column headers! The matching script needs these exact header names to work properly.

### Step 3: Run the Matching Script

1. Click on Extensions in the top menu
2. Select Apps Script

![SCREENSHOT 3: Show the Google Sheets menu with Extensions > Apps Script highlighted](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20150652.jpg)

3. A new tab will open showing the matching script code. You don't need to understand the code!

![SCREENSHOT 4: Show the Apps Script editor with the code visible](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20150839.jpg)

4. Click the Run button (▶️ icon)

[SCREENSHOT 5: Show the Apps Script editor with the Run button highlighted]

5. The first time you run the script, you'll see a permissions request:

[SCREENSHOT 6: Show the "Authorization required" dialog]

6. Click Review Permissions
7. Select your Google account when prompted

[SCREENSHOT 7: Show the "Choose an account" dialog]

8. You'll see a warning that says "Google hasn't verified this app" - this is normal for custom scripts. Click Advanced

[SCREENSHOT 8: Show the "Google hasn't verified this app" screen with "Advanced" link highlighted]

9. Click Go to [Your Project Name] (unsafe)

[SCREENSHOT 9: Show the screen with the "Go to [Project Name] (unsafe)" link highlighted]

10. Click Allow to give the script permission to access your spreadsheet

[SCREENSHOT 10: Show the permissions dialog with "Allow" button highlighted]

### Step 4: View Your Matches

1. After running the script, go back to your spreadsheet
2. Click on the "Matches" tab at the bottom

[SCREENSHOT 11: Show the spreadsheet with the "Matches" tab highlighted]

3. You'll see all your mentor-mentee matches listed here!

[SCREENSHOT 12: Show the Matches sheet with results]
Tips for Success

Make sure each college has at least one mentor and one mentee - otherwise, students from that college won't get matched
Double-check spelling of college names - "Stanford University" and "Stanford" would be treated as different match categories
Run the script again any time you add new participants
If you need to start over, just clear the "Matches" sheet and run the script again
