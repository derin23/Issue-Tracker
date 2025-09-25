# Issue Tracker

A simple, client-side web application for tracking and managing issues. Built with vanilla JavaScript, HTML5, and Bootstrap 4, this application provides an intuitive interface for creating, viewing, updating, and deleting issues.

## Features

- **Create Issues**: Add new issues with description, severity level, and assignee
- **View Issues**: Display all issues in a clean, organized list
- **Update Status**: Mark issues as closed when resolved
- **Delete Issues**: Remove issues that are no longer needed
- **Persistent Storage**: All data is stored locally using browser's localStorage
- **Responsive Design**: Mobile-friendly interface using Bootstrap 4

## Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES5)
- **UI Framework**: Bootstrap 4.1.3
- **JavaScript Libraries**:
  - jQuery 3.3.1 (slim)
  - Chance.js (for generating unique IDs)
  - Popper.js 1.14.3
- **Storage**: Browser localStorage (client-side persistence)

## Installation

1. **Clone or download** this repository to your local machine
2. **Open** the `index.html` file in your web browser
3. **That's it!** No additional setup or installation required

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- No server setup required - runs entirely in the browser

## Usage

### Adding a New Issue

1. Fill out the form in the "Add New Issue" section:
   - **Description**: Enter a detailed description of the issue
   - **Severity**: Select from Low, Medium, or High
   - **Assigned To**: Enter the name of the person responsible
2. Click the **Add** button to create the issue

### Managing Issues

Each issue card displays:

- **Issue ID**: Unique identifier (auto-generated)
- **Status**: Current status (Open/Closed)
- **Description**: Issue details
- **Severity**: Priority level
- **Assigned To**: Responsible person

### Available Actions

- **Close**: Mark an issue as resolved (changes status to "Closed")
- **Delete**: Permanently remove an issue from the tracker

## File Structure

```
Issue-Tracker/
├── index.html          # Main HTML file with UI structure
├── main.js            # JavaScript logic and functionality
└── README.md          # This documentation file
```

## Code Overview

### Main Functions

- `saveIssue(e)`: Handles form submission and creates new issues
- `fetchIssues()`: Retrieves and displays all issues from localStorage
- `setStatusClosed(id)`: Updates issue status to "Closed"
- `deleteIssue(id)`: Removes an issue from storage

### Data Structure

Issues are stored as JavaScript objects with the following structure:

```javascript
{
  id: "unique-guid",
  description: "Issue description",
  severity: "Low|Medium|High",
  assignedTo: "Assignee name",
  status: "Open|Closed"
}
```

## Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Data Persistence

All issue data is stored in the browser's localStorage, which means:

- Data persists between browser sessions
- Data is specific to each browser/device
- No server or database required
- Data can be cleared by clearing browser data

## Contributing

This is a simple demonstration project. Feel free to fork and modify for your own use cases.

## License

This project is open source and available under the [MIT License](LICENSE).

## Author

Created by **Derin Joseph** - [derinjoseph.com](https://derinjoseph.com)

---

_Note: This application runs entirely in the browser and does not require any server setup or external dependencies beyond what's loaded via CDN._
