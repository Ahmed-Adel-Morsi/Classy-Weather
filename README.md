# Classy Weather

A React weather forecast app that fetches geocoding and daily forecast data from Open-Meteo APIs.

This project is part of my practice work while reviewing React fundamentals through Jonas Schmedtmann’s course.

## Live Demo

- GitHub Pages: https://ahmed-adel-morsi.github.io/Classy-Weather

## Features

- Search weather by city name.
- Resolve city/country using geocoding API.
- Display a multi-day forecast with weather icons and min/max temperatures.
- Persist last searched location in local storage.
- Responsive, minimal single-page UI.

## Tech Stack

- React `19.2.4`
- React DOM `19.2.4`
- Create React App (`react-scripts` `5.0.1`)
- Testing Library packages (preconfigured by CRA)
- Deployment via `gh-pages` `6.3.0`

## APIs Used

- Geocoding: `https://geocoding-api.open-meteo.com/v1/search`
- Forecast: `https://api.open-meteo.com/v1/forecast`

## Project Structure

```text
.
├── public/
├── src/
│   ├── App-v1.js
│   ├── App-v2.js
│   ├── App.js
│   ├── index.css
│   └── index.js
├── build/
├── package.json
└── README.md
```

## App Versions

This repo keeps three versions of the main app implementation to track learning progression:

- `src/App-v1.js`:
  - Class-based components.
  - Manual trigger button (`Get weather`) for fetching.
  - Basic async fetch flow and rendering.

- `src/App-v2.js`:
  - Class-based components with lifecycle methods.
  - Auto-fetch on location change (`componentDidUpdate`).
  - Local storage persistence introduced.

- `src/App.js` (current active version):
  - Functional components with Hooks (`useState`, `useEffect`).
  - Auto-fetch on location updates.
  - Modularized input/weather/day rendering.
  - Cleaner modern React approach.

## Getting Started

### Prerequisites

- Node.js 18+ (recommended)
- npm

### Install

```bash
npm install
```

### Run in Development

```bash
npm start
```

Open `http://localhost:3000`.

### Run Tests

```bash
npm test
```

### Build for Production

```bash
npm run build
```

### Deploy to GitHub Pages

```bash
npm run deploy
```

## What I Learned

- Building the same feature with both class components and Hooks clarified the practical trade-offs between lifecycle methods and `useEffect`.
- Managing async API flows improved my handling of loading states, error boundaries, and conditional rendering.
- Persisting search input with local storage reinforced state synchronization patterns in React apps.
- Iterating from `App-v1.js` to `App.js` improved my component structure and code readability.

## Credits

- Course inspiration and learning path: Jonas Schmedtmann — _The Ultimate React Course_.
- Built as part of reviewing and strengthening my React knowledge through this course.
