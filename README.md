# KSEL Match Day Hub - README

## Overview
The KSEL Match Day Hub is a comprehensive web-based tournament management system designed for the Kern Schools/Scholastic Esports League weekly Fortnite competitions. It provides real-time coordination tools for tournament administrators and live schedule viewing for coaches and players.

**Students and Coaches:** Access the form at: [[https://erikmadams.github.io/ksel-fortnite-results](https://erikmadams.github.io/ksel_match_day_hub/)]

## Features

### Dual Access System
- **Player/Coach View**: Live tournament schedule and countdown timer
- **Admin View**: Full tournament management controls and team assignment tools

### Real-Time Tournament Management
- Live bus scheduling across two battle bus schedules (A & B)
- Dynamic team assignment with CSV upload support
- Real-time status updates visible to all participants
- Countdown timer for tournament start

### Visual Status System
Buses display different colors based on their current state:
- **Light Gray (Pending)**: Bus created but missing match key or teams
- **Yellow/Gold (Ready)**: Bus has both match key and teams assigned  
- **Light Green (Active)**: Bus has been launched in Fortnite
- **Light Red (Completed)**: 5 minutes have passed since launch

## Access URLs

### Player/Coach View
```
https://erikmadams.github.io/ksel_match_day_hub/
```
Shows live tournament schedule, countdown timer, and bus status updates.

### Admin View
```
https://erikmadams.github.io/ksel_match_day_hub/#admin
```
Full tournament management interface with all administrative controls.

## Admin Functions

### Bus Management
- **Add Bus**: Create new battle buses with custom names and launch times
- **Schedule Assignment**: Automatically sorts buses by time within Schedule A (3:30 release) or B (4:00 release)
- **Individual Bus Controls**: Each bus has dedicated team assignment and removal options

### Team Assignment
Two methods for assigning teams to buses:

#### Manual Entry
- Type team names directly into text area (one per line)
- Real-time team count display
- Immediate save to bus assignment

#### CSV Upload
- Upload CSV files with team names in first column
- Header row automatically ignored
- Preview functionality before saving
- Automatic parsing and validation

### Match Key Management
- Set unique match keys (Fortnite lobby codes) for each bus
- Match keys can be added/updated at any time
- Keys are hidden until set by administrator
- Real-time display updates to all viewers

### Launch Controls
- Manual launch checkboxes for each bus
- Launch timestamp tracking
- Automatic status progression (Active → Completed)
- 5-minute completion timer

### Countdown Timer
- Set target date/time for tournament start
- "Set to Next Thursday 7:00 PM" quick option
- Real-time countdown display
- Visible to all participants when enabled

## Tournament Workflow

### Pre-Tournament Setup
1. Access admin view using admin URL
2. Create buses for both schedules with names and times
3. Assign teams to each bus (manual entry or CSV upload)
4. Set countdown timer for tournament start
5. Set match keys when ready to release lobby codes

### During Tournament
1. Monitor bus status in admin view
2. Launch buses by checking "Launch Bus" when deployed in Fortnite
3. Status automatically updates for all participants
4. Buses turn green (active) then red (completed) after 5 minutes

### For Participants
1. Access player view using standard URL
2. View live schedule and countdown timer
3. See real-time status updates as buses are prepared and launched
4. Access match keys and team assignments when available

## Data Management

### Google Sheets Integration
The system uses Google Sheets for real-time data synchronization:
- Admin changes automatically save to Google Sheets
- Player views poll for updates every 5 seconds
- Ensures all participants see live tournament data
- Provides backup and persistence across sessions

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

### Google Sheets Configuration
1. Create Google Sheet with tournament data structure
2. Deploy Google Apps Script for API endpoints
3. Update HTML configuration with script URLs
4. Test read/write functionality

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
- Lucide icon integration

## Support
For technical support or feature requests, contact the KSEL tournament operations team.

## Version History
- v2.0: Google Sheets integration, enhanced team assignment, visual status system
- v1.0: Initial release with basic bus scheduling and countdown timer

## License
Developed for Kern Schools/Scholastic Esports League internal use.
