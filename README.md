# Clockface

A mesmerizing digital clock display where each digit is composed of tiny animated clock faces. The project creates a unique visual effect by using miniature clocks as "pixels" to form numbers that show the current time in HH:MM:SS format.

## Description

This project displays the current time using a creative approach - each digit (0-9) is rendered as a 4x6 grid of small clock faces. The clock hands on each mini-clock are positioned at specific angles to create the visual shape of the digit. As time changes, all the clock hands smoothly animate to their new positions, creating a fluid transition between digits.

### Features

- **Real-time clock display** - Shows hours, minutes, and seconds
- **Smooth animations** - Clock hands transition smoothly between positions using CSS transitions
- **Responsive design** - Adapts to different screen sizes with media queries
- **No build tools required** - Runs directly in the browser without babel or webpack
- **Modern React** - Uses React 19 with hooks via ESM imports from esm.sh

## How It Works

Each digit (0-9) is defined as a pattern of 24 mini-clocks arranged in a 4x6 grid. Each clock has:
- An **hour hand** positioned at a specific angle (0-360°)
- A **minute hand** positioned at a specific angle (0-360°)

By carefully positioning these hands at strategic angles (horizontal, vertical, diagonal), the clocks collectively form recognizable digit shapes. The app updates every second to display the current time.

## Project Structure

```
clockface/
├── index.html    # Main HTML file with root element
├── index.js      # React app with clock logic and digit patterns
├── style.css     # Styling for clocks and layout
└── README.md     # This file
```

## Usage

Simply open `index.html` in a modern web browser. No installation or build process required.

Alternatively, you can serve it with any static file server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js http-server
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

## Technical Details

- **React**: Uses React 19 with hooks (useState, useEffect, useRef)
- **Module imports**: Leverages ESM imports from esm.sh CDN
- **No JSX**: Uses `React.createElement` for browser compatibility without transpilation
- **CSS custom properties**: Uses CSS variables for dynamic styling and animations
- **Angle normalization**: Implements smart angle calculations to ensure clock hands take the shortest rotation path

## Browser Compatibility

Works in all modern browsers that support:
- ES6+ modules
- CSS custom properties
- CSS transitions
- Modern React features

## Credits

Inspired by and based on the original concept and code by [EntropyReversed](https://codepen.io/EntropyReversed) on CodePen.

## License

MIT
