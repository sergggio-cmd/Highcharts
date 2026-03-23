# Highcharts Data Visualization

Interactive data visualization module for FOB Arab Gulf - OPIS Carbon Offset NGL/LPG Index using Highcharts.

## Live Demo

https://sergggio-cmd.github.io/Highcharts/

## Features

### Dual View Modes
- **Normal View (662px)**: Full visualization with 6 data categories
- **Compact View (326px)**: Condensed layout with 3 data categories

### Interactive Controls
- **Refresh Button**: Updates chart data with smooth animations
- **View Toggle**: Switch between Normal and Compact views via dropdown menu
- **Animated Transitions**: Smooth fade-in/fade-out effects when changing views

### Design System
Built with **DJ Platform Library Design Tokens**:
- Typography: Inter font family
- Color palette: Blue primary (#1067f4), Blue secondary (#1493df), Gray (#6f6f81)
- Spacing system: 4px base unit
- Border radius: Consistent rounded corners (4-12px)
- Elevation: Shadow tokens for depth

## Tech Stack

- **Highcharts 11.x**: Column chart with custom styling
- **Vanilla JavaScript**: No frameworks, pure JS for performance
- **CSS Custom Properties**: Design token system
- **Google Fonts**: Inter font family (400, 500, 600 weights)

## Project Structure

```
Highcharts/
├── index.html           # Main application file
├── highcharts.js        # Highcharts library (v11.x)
├── highcharts.json      # Configuration/data file
├── test.html            # Testing file
└── README.md            # Documentation
```

## How to Use

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/sergggio-cmd/Highcharts.git
cd Highcharts
```

2. Serve the files with any HTTP server:
```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve

# VS Code Live Server extension
# Right-click index.html > Open with Live Server
```

3. Open browser at `http://localhost:8000`

### Usage

1. **Refresh Data**: Click the refresh icon (top-right) to update chart values
2. **Change View**: Click the three-dot menu icon and select:
   - "Normal view (662px)" - Full 6-bar chart
   - "Compact view (326px)" - Condensed 3-bar chart

## Chart Configuration

### Data Structure
- **X-Axis**: Time periods (May 1 - Oct 1 for Normal, Bar 1-3 for Compact)
- **Y-Axis**: NYMEX Differentials (cts/gal), range -5 to 10
- **Series**: 3 data series with distinct colors
  - USGC ULSD Differential (Blue #1067f4)
  - USGC ULSD Differential (Light Blue #1493df)
  - USGC ULSD Differential (Gray #6f6f81)

### Animations
- **Duration**: 300ms cubic-bezier easing
- **View Transitions**: 500ms synchronized fade-out/fade-in
- **Tooltip**: Positioned above bars with 8px border-radius

## Deployment

### GitHub Pages

The project is automatically deployed to GitHub Pages from the `gh-pages` branch.

**Deploy updates:**

1. Make changes in `main` or `feature/bar-chart` branch
2. Merge to `gh-pages`:
```bash
git checkout gh-pages
git merge main  # or feature/bar-chart
git push origin gh-pages
```

3. Changes will be live in 1-2 minutes at:
   https://sergggio-cmd.github.io/Highcharts/

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Modern mobile browsers

## Design Tokens Reference

| Token | Value | Usage |
|-------|-------|-------|
| `--content-base` | #1a222b | Primary text |
| `--content-subtle` | #778694 | Secondary text |
| `--surface-foreground` | #ffffff | Card background |
| `--surface-background` | #f6f7f8 | Page background |
| `--chart-blue-primary` | #1067f4 | Series 1 color |
| `--chart-blue-secondary` | #1493df | Series 2 color |
| `--chart-gray` | #6f6f81 | Series 3 color |
| `--elevation-sm` | 0px 2px 6px rgba(0,0,0,0.09) | Card shadow |

## License

MIT

## Author

Sergio Entrena
