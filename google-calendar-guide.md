# Google Calendar Setup Guide for Community Hall Booking System

This guide will walk you through setting up your Google Calendar for the community hall booking system.

## Creating a Dedicated Google Calendar

1. Go to [Google Calendar](https://calendar.google.com/)
2. In the left sidebar, find "Other calendars" and click the "+" button
3. Select "Create new calendar"
4. Fill in the details:
   - Name: "Community Hall Bookings"
   - Description: "Calendar for all community hall bookings and reservations"
   - Time zone: Select your local time zone (e.g., Australia/Melbourne)
5. Click "Create calendar"

## Configuring Calendar Settings

### Basic Settings
1. Find your new calendar in the left sidebar
2. Click the three dots next to it and select "Settings and sharing"
3. Under "General settings," you can customize:
   - Calendar name and description
   - Calendar time zone
   - Customize the calendar's display color

### Access Permissions
1. In the calendar settings, scroll to "Share with specific people"
2. Click "Add people" and add the email addresses of any administrators who should have full access
3. Set their permission level to "Make changes and manage sharing"
4. For public viewing (read-only):
   - Scroll to "Access permissions for events"
   - Check "Make available to public"
   - Set the permission to "See all event details"

### Getting the Calendar ID for Website Integration
1. Scroll down to "Integrate calendar"
2. Find the "Public URL to this calendar" section
3. Copy the Calendar ID, which looks something like:
   `abcdefg123456@group.calendar.google.com`
4. In your `index.html` file, replace `YOUR_CALENDAR_ID` with this ID

## Setting Up Event Notifications
1. In the calendar settings, scroll to "Event notifications"
2. Click "Add notification" to set up email or notification preferences
3. Choose when you want to be notified about upcoming events

## Calendar Appearance on Your Website
The calendar on your website can be customized by modifying the iframe URL parameters:

```html
<iframe src="https://calendar.google.com/calendar/embed?src=YOUR_CALENDAR_ID&ctz=YOUR_TIMEZONE&mode=MONTH&showTitle=0&showNav=1&showDate=1&showPrint=0&showTabs=1&showCalendars=0" style="border: 0" width="100%" height="600" frameborder="0" scrolling="no"></iframe>
```

You can modify these parameters:
- `mode=MONTH` - Display options: MONTH, WEEK, AGENDA
- `showTitle=0` - 0 hides the title, 1 shows it
- `showNav=1` - 1 shows navigation controls, 0 hides them
- `showDate=1` - 1 shows the current date, 0 hides it
- `showPrint=0` - 0 hides the print button, 1 shows it
- `showTabs=1` - 1 shows day/week/month tabs, 0 hides them
- `showCalendars=0` - 0 hides other calendars list, 1 shows them

## Managing Bookings

### Adding Events Manually
1. After approving a booking request from your Google Form:
   - Go to your Google Calendar
   - Click on the date and time for the booking
   - Create a new event with details from the booking request
   - Set the event visibility to "Public" so it appears on the website calendar
   - Add any notes or special requirements in the event description
   - Save the event

### Color Coding Different Event Types
You can use color coding to differentiate between different types of bookings:
1. When creating or editing an event, click the color indicator at the top
2. Select a color that corresponds to the type of event:
   - For example: Blue for community meetings, Green for private events, Red for maintenance, etc.
3. Create a color key and include it in your website content for visitors to understand

### Setting Up Recurring Events
For regular bookings (e.g., weekly club meetings):
1. Create a new event as usual
2. Click "Does not repeat" to open the recurrence menu
3. Select the appropriate recurrence pattern (daily, weekly, monthly, etc.)
4. Set an end date for the recurring booking if applicable
5. Save the event

## Connecting with Google Forms
When you receive a booking request through your Google Form:
1. Review the details in your connected Google Sheet
2. If approved, manually add the event to the calendar
3. Send a confirmation email to the requester with the booking details
4. If rejected, notify the requester with an explanation

## Embedding the Calendar on Your Website
The calendar iframe code has already been added to your website, but you may want to customize it further:

1. Adjust the size of the iframe by changing the `width` and `height` attributes
2. Modify the display options using the URL parameters as described above
3. Consider adding additional views or calendar tabs for different types of bookings

## Best Practices
1. Review the calendar regularly to ensure all bookings are accurate
2. Set up Google Calendar notifications for new bookings
3. Perform a monthly audit to ensure all approved form submissions have been added to the calendar
4. Consider creating a separate "Pending" calendar for unconfirmed bookings
5. Back up your calendar data periodically by exporting events

---

This concludes the Google Calendar setup guide for your community hall booking system.