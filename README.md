# KSEL Match Day Hub

A comprehensive tournament management platform for the Kern Schools/Scholastic Esports League (KSEL) Fortnite tournaments. This hub provides real-time battle bus scheduling, team management, and live match coordination across 28 local schools.

## Features

### Player/Coach Interface (Default View)
- **Real-time Battle Bus Schedules** - View upcoming matches across two tournament brackets
- **Live Status Updates** - Color-coded bus status (Yellow: Upcoming, Green: Active, Gray: Completed)  
- **Match Passwords** - Instantly accessible custom match passwords for each bus
- **Team Assignments** - See which teams are assigned to each battle bus
- **Current Time Display** - Always know the current time for match coordination

### Admin Control Panel (`?view=admin`)
- **Manual Launch Control** - Check boxes to manually launch buses and trigger status changes
- **Dual Schedule Management** - Manage Schedule A and Schedule B independently
- **Team Management** - Assign and reassign teams across different buses
- **Bus Management** - Add, remove, and clear buses with custom passwords
- **Real-time Coordination** - Changes instantly reflect in the player view
- **Tournament Statistics** - Overview of total teams, buses, and status counts

## Battle Bus System

### Status Management
- **Upcoming (Yellow)** - Default state before admin launches the bus
- **Active (Green)** - When admin manually checks the launch box
- **Completed (Gray)** - Automatically changes 7 minutes after launch

### Schedule Organization
- **Schedule A & B** - Two independent tournament brackets
- **High Capacity** - Supports up to 25 teams per bus without scroll issues
- **Time Format** - 12-hour time display for better readability

## Technical Stack

- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **Styling:** Tailwind CSS for responsive design
- **Icons:** Lucide Icons for professional UI elements
- **Deployment:** GitHub Pages for reliable hosting
- **Data Storage:** Client-side JSON for real-time updates

## KSEL Integration

This hub integrates with the broader KSEL tournament ecosystem:

- **Results Entry System** - Link to match results collection
- **Analytics Dashboard** - Connection to performance leaderboards
- **School Network** - Serves 28 schools across Kern County
- **Brand Consistency** - Official KSEL styling and logo integration

## Responsive Design

- **Mobile Optimized** - Works on phones, tablets, and desktops
- **Touch Friendly** - Easy interaction on all device types
- **Professional Appearance** - Tournament-grade interface design
- **Fast Loading** - Optimized for quick access during events

## Setup & Deployment

### Local Development
```bash
# Clone the repository
git clone https://github.com/erikmadams/ksel_match_day_hub.git

# Navigate to directory
cd ksel_match_day_hub

# Open in browser
open index.html
```

### GitHub Pages Deployment
1. Push your changes to the main branch
2. Enable GitHub Pages in repository settings
3. Set source to "Deploy from a branch" - main branch
4. Your site will be available at `https://yourusername.github.io/ksel_match_day_hub/`

## Usage Instructions

### For Tournament Administrators
1. Access the admin panel: `your-url/?view=admin`
2. Add buses using the "Add Bus" buttons for each schedule
3. Assign teams through the "Edit" button in Team Management
4. Launch buses by checking the launch boxes during tournaments
5. Monitor status through the Tournament Status panel

### For Players and Coaches
1. Visit the main URL (no parameters needed)
2. Check your assigned bus and match password
3. Monitor bus status colors for timing
4. Join matches when your bus shows green (active)

## Tournament Workflow

1. **Pre-Tournament Setup** (Admin)
   - Create battle bus schedules for both brackets
   - Assign teams to appropriate buses
   - Set custom match passwords

2. **Live Tournament Management** (Admin)
   - Launch buses by checking launch boxes
   - Monitor team assignments and status
   - Coordinate across multiple matches

3. **Player Participation** (Teams)
   - Access schedules through public URL
   - Use match passwords to join custom games
   - Follow color-coded status for timing

## KSEL Tournament System

Part of the comprehensive KSEL esports infrastructure:
- **Match Results Entry** - Collect player statistics and team performance
- **Analytics Dashboard** - Season standings and playoff qualification tracking
- **Match Day Hub** - Real-time tournament coordination (this project)

## Contributing

This project is part of the Kern Schools/Scholastic Esports League infrastructure. For contributions or issues:

1. Create detailed issue reports
2. Follow existing code patterns and styling
3. Test across different devices and browsers
4. Maintain KSEL brand consistency

## License

Developed for the Kern Scholastic Esports League (KSEL) tournament infrastructure.

## Support

For technical issues or tournament support:
- Check the GitHub Issues page
- Contact KSEL tournament administrators
- Reference the integrated help documentation

---

**Built for KSEL** - Empowering competitive esports across Kern County schools
