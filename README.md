# Lottery Inventory — Shift Calculator

A modern, mobile-friendly web application for lottery retailers to calculate and track inventory, float sheets, and daily sales. Built with [Preact](https://preactjs.com/) and vanilla JavaScript, with a responsive design optimized for both desktop and mobile devices.

## Features

### 📊 Three Calculation Modes
- **Shift Data**: Track stock, activated tickets, and sold tickets to calculate closing inventory
- **Float Sheet**: Manage opening float inventory levels
- **Daily Sales**: Record and calculate daily sales revenue

### 💾 Data Persistence
- Automatic save to browser's localStorage
- Separate state management for each mode
- Metadata storage (date and cashier name)
- No backend required — works completely offline

### 📱 Responsive Design
- **Desktop**: Full table view with complete data visibility
- **Mobile**: Card-based carousel view for easy one-handed input
- Virtual numeric keypad optimized for data entry
- Smooth transitions between denominations

### 📤 Export & Print
- **CSV Export**: Download data for spreadsheet applications
- **Print to PDF**: Generate physical reports with formatting
- Properly formatted headers with date and cashier information

### 🎯 Real-Time Calculations
- Instant closing inventory calculations (Stock + Activated - Sold)
- Automatic value calculations (closing inventory × denomination)
- Error detection for negative inventory
- Running totals for all modes

### 🎨 Modern UI
- Dark theme with green accent colors
- Smooth animations and transitions
- Clear visual feedback for active inputs
- Error highlighting for invalid calculations
- Accessibility features (ARIA labels, semantic HTML)

## Quick Start

1. Open `index.html` in any modern web browser
2. Select your calculation mode (Shift Data, Float Sheet, or Daily Sales)
3. Choose your view: Table for full data, Card for mobile-optimized input
4. Enter data using the virtual keypad or by clicking cells
5. Export or print your report when complete

## Supported Denominations

The calculator supports lottery ticket denominations:
- $2, $3, $4, $5, $10, $20, $30, $50, $100

## Browser Support

- Chrome/Chromium (recommended)
- Firefox
- Safari
- Edge
- Any modern browser supporting ES6+ and localStorage

## Technical Details

### Technologies
- **Framework**: Preact 10.19.6 (lightweight React alternative)
- **Templating**: htm (JSX-like syntax)
- **Storage**: Browser localStorage API
- **CSS**: Modern CSS with CSS custom properties (variables)
- **Fonts**: Google Fonts (DM Mono, Sora)

### Architecture
- Single-page application (SPA) with no build step
- Modular component structure
- State management with React hooks
- Logic isolation for calculations

## Data Storage Keys

The application uses these localStorage keys:
- `lotto_v2_state`: Shift calculation data
- `lotto_v2_float_state`: Float sheet data
- `lotto_v2_sales_state`: Daily sales data
- `lotto_v2_meta`: Metadata (date, cashier)
- `lotto_v2_tab`: Currently active tab
- `lotto_v2_viewMode`: Currently active view mode

**Note**: Clearing browser data or localStorage will reset all entries.

## Keyboard & Input

- **Virtual Keypad**: Click buttons or use keyboard numbers
- **CLR**: Clear current field
- **DEL**: Delete last digit
- **Next**: Move to next field or denomination
- **Direct Click**: Click any cell to select it

## Troubleshooting

### Data disappeared after closing the browser
- Check browser privacy settings — localStorage may be disabled
- Try a different browser
- Ensure you're not in private/incognito mode

### Export doesn't work
- Check browser security settings
- Ensure pop-ups aren't blocked
- Try a different browser

### View toggle not working
- Try refreshing the page
- Clear localStorage by opening DevTools → Application → Clear All

## License

This project is open source and available for public use.

## Contributing

Found a bug or have a suggestion? Feel free to open an issue or submit a pull request!
