# match-mentees-and-mentors

[Match Mentees and Mentors Template](https://docs.google.com/spreadsheets/d/1JhOxsP6_pxdapIs9xdHRGP0hU6LoT1-oOISrJtPe69I/edit?usp=sharing)

This Google Sheet automatically matches mentees with mentors from the same college. This README will guide you through using the spreadsheet, even if you have no technical background.

## What This Tool Does
This spreadsheet:

- Automatically pairs mentees with mentors from the same college
- Ensures each mentee gets exactly 1 mentor
- Ensures each mentor is assigned to no more than 1 mentee
- Creates a clean "Matches" sheet showing all the pairings

## Getting Started
### Step 1: Access the Template

1. Open the Google Sheet template
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
5. The first time you run the script, you'll see a permissions request:

![SCREENSHOT 6: Show the "Authorization required" dialog](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20151024.jpg)

6. Click Review Permissions
7. Select your Google account when prompted

![SCREENSHOT 7: Show the "Choose an account" dialog](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20151145.jpg)

8. You'll see a warning that says "Google hasn't verified this app" - this is normal for custom scripts. Click Advanced

![SCREENSHOT 8: Show the "Google hasn't verified this app" screen with "Advanced" link highlighted](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20151314.jpg)

9. Click Go to [Your Project Name] (unsafe)

![SCREENSHOT 9: Show the screen with the "Go to [Project Name] (unsafe)" link highlighted](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20151420.jpg)

10. Click Allow to give the script permission to access your spreadsheet

![SCREENSHOT 10: Show the permissions dialog with "Allow" button highlighted](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20151540.jpg)

### Step 4: View Your Matches

1. After running the script, go back to your spreadsheet
2. Click on the "Matches" tab at the bottom

![SCREENSHOT 11: Show the spreadsheet with the "Matches" tab highlighted](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20151856.jpg)

3. You'll see all your mentor-mentee matches listed here!

![SCREENSHOT 12: Show the Matches sheet with results](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20152001.jpg)

## Tips for Success

- Make sure each college has at least one mentor and one mentee - otherwise, students from that college won't get matched
- Double-check spelling of college names - "Stanford University" and "Stanford" would be treated as different match categories
- Run the script again any time you add new participants
- If you need to start over, just clear the "Matches" sheet and run the script again

## Adjusting the Matching Ratio
You can change how many mentors each mentee gets, or how many mentees each mentor can support, by modifying two simple numbers in the script:

Click on Extensions > Apps Script again
Find these two lines near the top:
var MENTORS_PER_MENTEE = 1; // Number of mentors each mentee should have
var MAX_MENTEES_PER_MENTOR = 1; // Maximum number of mentees per mentor

Change the numbers to meet your needs:

To give each mentee 2 mentors: Change MENTORS_PER_MENTEE = 1 to MENTORS_PER_MENTEE = 2
To allow each mentor to support up to 3 mentees: Change MAX_MENTEES_PER_MENTOR = 1 to MAX_MENTEES_PER_MENTOR = 3

![SCREENSHOT 13: Show the Apps Script editor with these two variables highlighted, and arrows pointing to where the numbers can be changed](https://github.com/jonsiapno/match-mentees-and-mentors/blob/main/screenshots/Screenshot%202025-05-13%20152336.jpg)

Click Save and then Run to apply your changes

Example: If you have more mentees than mentors, you might set MAX_MENTEES_PER_MENTOR = 3 so each mentor can support multiple mentees.
