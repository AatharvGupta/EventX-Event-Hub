# EventX

EventX is a responsive college event management demo. Students can discover events, create a demo account, register for events, and view their attendance. Organizers can manage events, participants, and attendance.

## Run in Replit

Open the EventX preview to start using the site. The Replit workflow supplies the app's preview settings.

## Demo accounts

| Role | Email | Password |
| --- | --- | --- |
| Student | `student@eventx.com` | `student123` |
| Organizer / admin | `admin@eventx.com` | `admin123` |

You can also create a student account from the registration page.

## Demo data and privacy

Events, registrations, attendance, and demo account data are stored in this browser's local storage. They are not shared with other browsers or users, and clearing browser storage resets the demo. This frontend-only authentication is for demonstration and is not secure enough for real accounts or production use.

Event artwork is stored locally in `public/event-images/`; no image service or API key is required.

## Checks

From the workspace root:

```sh
pnpm --filter @workspace/eventx run typecheck
```

This frontend demo does not include a server, database, or real authentication service.
