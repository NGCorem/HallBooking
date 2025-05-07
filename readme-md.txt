# Community Hall Booking System

A simple and effective booking system for community halls built with Google services and GitHub Pages.

## Overview

This system uses a combination of:
- GitHub Pages for hosting a responsive website
- Google Calendar for availability display (read-only for public)
- Google Forms for booking requests
- Email notifications handled by Google
- Optional custom domain

## Setup Instructions

### 1. Google Calendar Setup

1. Create a new Google Calendar specifically for your community hall bookings
2. Go to Calendar Settings → Share with specific people → Add people
3. Add your email address with "Make changes and manage sharing" permissions
4. Under "Integrate calendar" section, copy your "Public URL to this calendar"
5. Replace the `YOUR_CALENDAR_ID` placeholder in the `index.html` file with your calendar ID
6. Set your timezone by replacing `YOUR_TIMEZONE` with your local timezone (e.g., `Australia/Melbourne`)

### 2. Google Form Setup

1. Create a new Google Form for booking requests with these fields:
   - Name (Short answer)
   - Email (Short answer)
   - Phone Number (Short answer)
   - Event Date (Date)
   - Start Time (Time)
   - End Time (Time)
   - Expected Number of Attendees (Short answer)
   - Event Description (Paragraph)
   - Additional Requirements (Paragraph)
   - Terms and Conditions Acceptance (Checkbox)

2. Go to Responses → Three dots menu → Select response destination → Create a new spreadsheet
3. Go to Form → Settings (gear icon) → Emails → Get email notifications for new responses
4. In the form editor, click "Send" → Copy the embed HTML
5. Replace the `YOUR_FORM_ID` placeholder in the `index.html` file with your form ID

### 3. GitHub Pages Setup

1. Create a new GitHub repository
2. Upload all the files from this project to your repository
3. Go to repository Settings → Pages
4. Under "Source", select "main" branch and click Save
5. Your site will be published at `https://yourusername.github.io/repository-name/`

### 4. Custom Domain (Optional)

1. Purchase a domain from a domain registrar
2. Go to your repository Settings → Pages → Custom domain
3. Enter your domain name and click Save
4. Configure your DNS settings according to GitHub's instructions

## Customization

- Edit the `index.html` file to modify the content and structure
- Adjust the styles in the `css/style.css` file to match your branding
- Modify the `js/script.js` file to add or change functionality

## Maintenance

- Booking requests will be automatically collected in your Google Spreadsheet
- You can manually add approved bookings to your Google Calendar
- Update your website content through GitHub as needed

## Support

For assistance with this system, please contact the system administrator.

---

Community Hall Booking System © 2025