# KSEL Match Day Hub - README

## Overview
The KSEL Match Day Hub is a comprehensive web-based tournament management system designed for the Kern Scholastic Esports League weekly Fortnite competitions. It provides real-time coordination tools for tournament administrators and live schedule viewing for coaches and players.

**Students and Coaches:** Access the Bus Dashboard at: [Match Day Hub](https://erikmadams.github.io/ksel_match_day_hub/)

## Features

### Dual Access System
- **Player/Coach View**: Live bus schedule and countdown timer
- **Admin View**: Full bus management controls and team assignment tools

### Real-Time Tournament Management
- Live bus scheduling across two battle bus schedules
- Schedule 'A' 3:30ish release time / Schedule 'B' 4:00ish release time
- Real-time status updates visible to all participants
- Countdown timer to let everyone know when the launches start for the week

### Visual Status System
Buses display different colors based on their current state:
- **Light Gray (Pending)**: Bus created but missing match key
- **Gold (Ready)**: Bus has match key assigned
- **Green (Active)**: Bus has been launched in Fortnite
- **Red (Completed)**: 5 minutes have passed since launch and match is in progress

Status color is driven entirely by the match key and launch checkbox — assigning teams to a bus does not change its color.

## Page Views

### Player/Coach View
Shows live tournament schedule, countdown timer, and bus status updates.

### Admin View
Full tournament management interface with all administrative controls.

## Admin Functions

### Bus Management
- **Add Bus**: Create new battle buses with custom names and launch times. New buses are added to the end of their schedule.
- **Edit Bus**: Click the pencil icon on any bus to update its name or launch time without deleting and recreating it — handy for reusing last week's buses.
- **Reorder Buses**: Click and drag a bus card to move it up or down within its schedule, or drag it into the other schedule's column to move it between Schedule A and Schedule B. Buses are no longer auto-sorted by time, so the order is entirely up to you.
- **Individual Bus Controls**: Each bus has dedicated edit, match key assignment, team assignment, and removal options.

### Team Assignment
- Assign teams to a bus via manual entry (one team name per line) or CSV upload
- Team list and count are shown on each bus card
- Teams can be added, changed, or cleared at any time and have no effect on a bus's status color

### Match Key Management
- Set unique match keys (Fortnite lobby codes) for each bus
- Match keys can be added/updated at any time
- Keys are hidden until set by administrator
- Real-time display updates to all viewers
- Match key is shown in a larger, bolder font on each bus card for easy reading at a glance

### Launch Controls
- Manual launch checkboxes for each bus
- Launch timestamp tracking
- Automatic status progression (Active → Completed)
- 5-minute completion timer

### Countdown Timer
- Set target date/time for tournament start
- "Set to Next Thursday at 4:15 PM" quick option
- Real-time countdown display
- Visible to all participants when enabled

## Match Day Workflow

### Pre-Match Day Setup
1. Set countdown timer for tournament start
2. Access admin view using admin URL
3. Reuse last week's buses by editing their names/times, or create new ones for both schedules
4. Reorder or move buses between schedules as needed
5. Assign teams to buses
6. Set match keys when ready to release lobby codes

### During Matches
1. Monitor bus status in admin view
2. Launch buses by checking "Launch Bus" when deployed in Fortnite
3. Status automatically updates for all participants
4. Buses turn green (active) then red (completed) after 5 minutes

### For Participants
1. Access player view using standard URL
2. View live schedule and countdown timer
3. See real-time status updates as buses are prepared and launched
4. Access match keys when available

### Local Storage Fallback
- Automatic fallback to browser storage if Google Sheets unavailable
- Maintains functionality during connectivity issues
- Seamless transition between storage methods

## Browser Compatibility
- Chrome (recommended)
- Safari
- Firefox
- Edge
- Mobile browsers supported

## Setup Requirements

### GitHub Pages Deployment
1. Upload HTML file to GitHub repository
2. Enable GitHub Pages in repository settings
3. Access via GitHub Pages URL
4. Cache control headers prevent stale content

## File Structure
```
ksel_match_day_hub.html - Main application file
README.md - This documentation
```

## Technical Features
- Responsive design for desktop and mobile
- Real-time polling for live updates
- CORS proxy handling for Google Sheets access
- LocalStorage backup system
- Cache control for reliable deployment
- Tailwind CSS styling
- Lucide icon integration, with a fallback so the page keeps working (clock, schedule, Google Sheets sync) even if the icon library fails to load

## Support
For technical support or feature requests, contact the KSEL leadership team.

## Version History
- v5.0: Restored team assignment (manual entry and CSV upload) with status color depending only on the match key; doubled the match key display size; simplified the header subtitle; changed the countdown quick-set option to 4:15 PM and fixed a bug where the countdown's target date could get stuck on "Loading..."; added an Edit Bus button for changing a bus's name/time in place; added drag-and-drop to reorder buses within a schedule or move them between Schedule A and B; removed automatic time-based sorting so bus order is fully manual; fixed a bug that could freeze the entire page if the icon library failed to load
- v4.0: Removed team assignment from buses and made adjustments to the timer
- v3.0: Real-time Google Sheets integration with live data sync, enhanced visual bus status system, dedicated match key management, CSV team upload, and 5-second polling updates
- v2.0: Google Sheets integration, enhanced team assignment, visual status system
- v1.0: Initial release with basic bus scheduling and countdown timer

## License
Developed for Kern Scholastic Esports League by LeagueHQ developers.  For KSEL internal use only.
