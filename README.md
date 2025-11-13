# WhatsApp Booking Appointment n8n Workflow

This repository contains an n8n workflow that automates appointment booking through WhatsApp. The workflow listens for booking messages sent to your WhatsApp business number, checks availability in your calendar, and confirms or reschedules appointments with customers automatically. It's ideal for services such as medical consultations, salons, or any business that takes bookings via WhatsApp.

## Features

- **Real‑time appointment requests**: Accepts incoming booking inquiries through WhatsApp using Twilio or WhatsApp Business API webhooks.
- **Availability checks**: Queries a connected calendar (e.g. Google Calendar, Outlook) or a dedicated scheduling service to find open time slots.
- **Automated confirmations & reminders**: Sends confirmation messages with appointment details and follow‑up reminders via WhatsApp.
- **Rescheduling & cancellations**: Provides alternative times and updates the calendar if a customer needs to reschedule or cancel.
- **Integration‑ready**: Can be extended to sync with CRM systems or take payments by connecting additional n8n nodes.

## Getting Started

### Prerequisites

- [n8n](https://n8n.io) self‑hosted or cloud.
- A WhatsApp Business API or Twilio WhatsApp account with valid credentials.
- Access to a calendar API or booking system (e.g. Google Calendar API).
- Node and API credentials configured in n8n.

### Importing the Workflow

1. Clone or download this repository.
2. In n8n, go to **Workflows** → **Import**, select `whatsapp booking appointment.json` from this repository, and upload it.
3. Update the credential nodes with your WhatsApp and calendar API keys.
4. Configure environment variables for secrets (e.g. `TWILIO_ACCOUNT_SID`, `TWILIO_AUTH_TOKEN`, `CALENDAR_API_KEY`, `BUSINESS_PHONE_NUMBER`).
5. Test the workflow by sending a booking request to your WhatsApp number.

### Customising

- Modify the time slot logic to align with your business hours and service durations.
- Update the message templates in the **WhatsApp** nodes to reflect your branding and tone.
- Integrate with a CRM or database to persist booking details by adding additional nodes.
- Add payment processing by connecting to services like Stripe or PayPal.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
