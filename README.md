# automated booking system

Automated booking system developed for client.
Upon receiving an appointment (via email confirmation), this system will:

- Automatically check availability of predefined rooms in order of preference.

- Book the earliest available room that matches the appointment time.

- Send confirmation via email.

- Log the booking and notify the business.

Problem: Current booking process is manual, repetitive, and error-prone. This slows down operations and increases the risk of double-booking or missing room availability.

Solution: A Python-based web automation script that mimics human interaction with the booking portal via either a headless browser or HTTP requests.

Room Booking Priorities
In order of preference:

["consult room 1", "consult room 2", "consult room 3",
"treatment room 1", "treatment room 2", "treatment room 3"]

Booking Form Requirements
To successfully submit a booking, the following fields must be completed:

- Room (dropdown)
- Type (e.g., Consultation, Treatment)
- Date (formatted input or calendar picker)
- Time (start and end time selection)
- Guest (patient name)

### Discovery & Requirements Gathering

Tasks:

- [ ] Confirm URL and login process for the Untill Portal.

- [ ] Identify HTML structure for booking form and room availability interface.

- [ ] Determine any CAPTCHA, anti-bot protections, or session handling mechanisms.

- [ ] Identify email service used (for receiving confirmations).

- [ ] Choose deployment schedule: real-time trigger vs batch job.

### Automation

Tasks:

- [ ] Set up headless browser automation using Playwright or Selenium.

- [ ] Implement login and session handling.

- [ ] Parse available room slots from DOM (or HTML requests).

- [ ] Loop through room preferences and select earliest available.

- [ ] Fill out booking form and submit.

- [ ] Confirm success from UI or email response.

- [ ] Store booking in local file or DB.

### CLI/Script Integration

Tasks:

- [ ] Build a Python CLI or script entry point (e.g., book_room.py)

- [ ] Add error handling & retry logic for failed submissions.

- [ ] Add logging to track success/failure.

### Notifications & Logging

Tasks:

- [ ] Parse confirmation email for details.

- [ ] Optional: forward confirmation to your address or notify via Slack/Email.

- [ ] Store logs with timestamped records of booking attempts.

### Testing & Debugging

Tasks:

- [ ] Test with demo account.

- [ ] Create unit tests for modular functions (login, room parsing, booking).

- [ ] Manual validation across date/time edge cases.

### Deployment & Maintenance

Tasks:

- [ ] Deploy on a local server, Raspberry Pi, or cloud VM.

- [ ] Extra: Build lightweight dashboard or log viewer.
