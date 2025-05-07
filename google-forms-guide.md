# Google Forms Setup Guide for Community Hall Booking System

This guide will walk you through setting up your Google Form for collecting booking requests for your community hall.

## Creating a New Google Form

1. Go to [Google Forms](https://forms.google.com/)
2. Click the "+" button to create a new blank form
3. Give your form a title: "Community Hall Booking Request"
4. Add a description: "Please complete this form to request a booking for our community hall"
5. Customize the header color and theme to match your branding (optional)

## Setting Up Form Sections and Questions

### Personal Information Section
1. Click "Add section" and title it "Personal Information"
2. Add the following questions:
   
   - **Full Name**
     - Question type: Short answer
     - Required: Yes
   
   - **Email Address**
     - Question type: Short answer
     - Required: Yes
     - Validation: Email
   
   - **Phone Number**
     - Question type: Short answer
     - Required: Yes
   
   - **Organization (if applicable)**
     - Question type: Short answer
     - Required: No

### Booking Details Section
1. Add another section titled "Booking Details"
2. Add the following questions:
   
   - **Event Name/Type**
     - Question type: Short answer
     - Required: Yes
   
   - **Event Date**
     - Question type: Date
     - Required: Yes
   
   - **Start Time**
     - Question type: Time
     - Required: Yes
   
   - **End Time**
     - Question type: Time
     - Required: Yes
   
   - **Setup Time Required**
     - Question type: Multiple choice
     - Options: "No setup time needed", "30 minutes", "1 hour", "2 hours"
     - Required: Yes
   
   - **Expected Number of Attendees**
     - Question type: Short answer
     - Required: Yes
     - Validation: Number (between 1-120)
   
   - **Event Description**
     - Question type: Paragraph
     - Required: Yes

### Additional Requirements Section
1. Add another section titled "Additional Requirements"
2. Add the following questions:
   
   - **Facilities Needed**
     - Question type: Checkboxes
     - Options: "Kitchen", "Projector", "Sound System", "Tables", "Chairs"
     - Required: No
   
   - **Any Special Requirements**
     - Question type: Paragraph
     - Required: No

### Terms and Conditions Section
1. Add a final section titled "Terms and Conditions"
2. Add the following questions:
   
   - **Terms Acceptance**
     - Question type: Checkbox
     - Option: "I have read and agree to the Terms and Conditions for hall usage"
     - Required: Yes
   
   - **Cleanup Agreement**
     - Question type: Checkbox
     - Option: "I understand that I am responsible for cleaning the hall after the event"
     - Required: Yes

## Form Settings and Configuration

### Connect to Google Sheets
1. Click the "Responses" tab at the top of the form
2. Click the Google Sheets icon (looks like a green spreadsheet)
3. Select "Create a new spreadsheet"
4. Click "Create" to generate a new spreadsheet for responses
5. The spreadsheet will open in a new tab - you may want to rename it "Community Hall Booking Requests"

### Set Up Email Notifications
1. In the "Responses" tab, click the three dots menu
2. Select "Get email notifications for new responses"
3. Confirm your email or add other administrator emails

### Add a Confirmation Message
1. Click the Settings gear icon at the top
2. Under "Presentation" tab, customize the confirmation message:
   "Thank you for your booking request. We will review your submission and contact you within 2 business days to confirm your booking."

### Set Access Permissions
1. Still in Settings, go to the "Responses" tab
2. Under "Requires sign-in", you can choose:
   - If you want respondents to be limited to one response (requires Google sign-in)
   - Or allow anyone to submit without signing in (more user-friendly but may allow duplicate submissions)

### Form Visibility and Distribution
1. Click the "Send" button at the top right
2. You'll see several options to share your form:
   - Via email
   - Using a link
   - Via HTML embed code for your website

3. For your website, click the embed icon (looks like `<>`)
4. Copy the provided iframe HTML code
5. In your website's `index.html` file, replace the placeholder iframe in the "Book the Hall" section with this code

## Embedding the Form on Your Website
The form iframe code should look something like this:

```html
<iframe src="https://docs.google.com/forms/d/e/YOUR_FORM_ID/viewform?embedded=true" width="100%" height="800" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
```

Replace `YOUR_FORM_ID` in your website's HTML with the actual ID from the iframe code.

## Managing Responses

### Reviewing Submissions
1. You can view responses in two ways:
   - Directly in the Google Form by clicking the "Responses" tab
   - In the connected Google Sheet for more detailed data management

2. In the Google Sheet:
   - Each row represents a booking request
   - Columns correspond to the questions in your form
   - Timestamps are automatically added

### Processing Bookings
1. Create a new column in your Google Sheet called "Status"
2. As booking requests come in, update their status:
   - "Pending" - Initial state
   - "Approved" - Booking confirmed
   - "Rejected" - Booking declined
   - "Cancelled" - Booking was confirmed but later cancelled

3. You can use conditional formatting to color-code rows based on status

### Creating an Automated Response Workflow (Optional Advanced Setup)
Using Google Apps Script (accessible from your Google Sheet):
1. Click Extensions → Apps Script
2. Create a script to send automatic emails when you change a booking status
3. Example script templates are available online for this purpose

## Best Practices
1. Review your form regularly and update questions as needed
2. Check for any validation errors or unclear instructions
3. Process booking requests promptly
4. Consider setting up a separate email address just for booking-related communications
5. Periodically export and backup your response data

---

This concludes the Google Forms setup guide for your community hall booking system.