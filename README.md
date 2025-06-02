# Meeting-Room-Status-Dashboard-google-workspace
# 🏢 Meeting Room Status Dashboard

A sleek and auto-refreshing Google Apps Script web app that shows **free/busy status** for multiple meeting rooms, using Google Calendar. Designed for office displays, tablets, or TVs — with thoughtful UI touches and privacy features.

---

## ✨ Features

- ✅ Displays live room availability (Free / Busy)
- 📆 Shows current and next booking (with time range)
- 🔒 Obfuscates email of event creators
- 🔐 Respects “Private” visibility on events
- 🕐 Clock display with local time and timezone label
- 📅 Shows full date and calendar week number
- 🔁 Auto-refreshes every 5 minutes
- 🌄 Beautiful full-screen background (from Google Drive)

---
## 🛠️ How It Works

This app uses:
- **Google Calendar API (via Apps Script)** to fetch upcoming events for room calendars
- A dynamic HTML page with embedded JavaScript to display status and update the clock
- Public image from **Google Drive** as the background

---

## 🧩 Setup Instructions

### 1. Prepare Room Calendars
Ensure your rooms are **Google Workspace resource calendars**. Get their email addresses (example: `c_123abc@resource.calendar.google.com`).

### 2. Open Google Apps Script

1. Visit [script.new](https://script.new)
2. Paste in the full code from https://github.com/jameaton/Meeting-Room-Status-Dashboard-google-workspace/blob/main/full%20code 
3. Update the `ROOM_CALENDARS` array with your actual room names and IDs:
   ```js
   const ROOM_CALENDARS = [
     { name: "Room A", id: "your_room_calendar_id" },
     ...
   ];
3. Deploy as Web App
Click Deploy → Manage deployments

Click New Deployment

Set access to "Anyone" or "Anyone within your org"

Copy the web app URL and open it in a browser or full-screen kiosk

🧠 Example Output
text
Copy
Edit
Room: Copenhagen
Status: Busy
Title: Strategy Sync
Time: 2:00 PM – 3:00 PM
Booked by: jan***@company.com

Next: Private meeting
Time: 3:30 PM – 4:00 PM
📷 Customize Appearance
🌄 Background
Update this line in the <style> section:

background: url('https://lh3.googleusercontent.com/d/IMAGE_ID=w1920') no-repeat center center fixed;
Upload your own image to Google Drive → Share → Replace IMAGE_ID with its file ID.

🔐 Permissions & Privacy
Only calendar event visibility and organizer data are used.

Private meetings display only the label “Private meeting”.

Email addresses are obfuscated (e.g., jan***@domain.com).

📦 Future Ideas
Slack/Chat status integration

QR booking links

Overrun alerts

Weekly meeting heatmaps

🧑‍💻 Maintainer
James Eaton
IT Engineer
Feel free to fork, improve, or raise issues!

📄 License
MIT — free to use, adapt, and share.
