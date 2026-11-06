# NextWork Web App

A small personal web app used for learning. Visitors can send the Owner a Contact Message, and the Owner gets a Notification for each one.

## Language

**Owner**:
The single person who runs this app and is the only recipient of Notifications.
_Avoid_: User, admin, recipient

**Visitor**:
Anyone who opens the app's page and may send a Contact Message.
_Avoid_: User, customer, sender

**Contact Message**:
A Visitor's name, email address, and message text, sent to the Owner through the contact form.
_Avoid_: Submission, feedback, inquiry, ticket

**Notification**:
A message delivered to the Owner telling them that a Contact Message has arrived and showing what it says. A Contact Message arriving is the only event that produces one.
_Avoid_: Alert, ping, event
