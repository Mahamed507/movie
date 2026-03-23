# 🎬 Movie App

A React application for discovering and saving your favorite movies, powered by the TMDB API.

## Features

- **Browse Popular Movies** — Loads trending movies on startup
- **Search** — Find any movie by title using the TMDB search API
- **Favorites** — Add or remove movies from your personal favorites list
- **Persistent Storage** — Favorites are saved to `localStorage` so they survive page refreshes

## Tech Stack

- **React** (with Hooks & Context API)
- **React Router v6** — client-side routing
- **TMDB API** — movie data and poster images
- **CSS Modules** — component-scoped styling

## Project Structure

```
src/
├── components/
│   ├── MovieCard.jsx       # Individual movie card with favorite toggle
│   └── NavBar.jsx          # Navigation bar
├── contexts/
│   └── MovieContext.jsx    # Global favorites state via Context API
├── pages/
│   ├── Home.jsx            # Browse & search movies
│   └── Favorites.jsx       # View saved favorites
├── services/
│   └── api.js              # TMDB API calls
└── css/                    # Component stylesheets
```

## Getting Started

### Prerequisites

- Node.js (v16+)
- A free [TMDB API key](https://www.themoviedb.org/settings/api)

### Installation

```bash
# Clone the repo
git clone https://github.com/your-username/movie-app.git
cd movie-app

# Install dependencies
npm install
```

### Configuration

Open `src/services/api.js` and replace the API key with your own:

```js
const API_KEY = "your_tmdb_api_key_here";
```

### Run Locally

```bash
npm start
```

Visit `http://localhost:3000` in your browser.

## Usage

| Action | How |
|---|---|
| Browse movies | Open the app — popular movies load automatically |
| Search | Type in the search bar and hit **Search** |
| Add to favorites | Click the ♥ button on any movie card |
| View favorites | Click **Favorite** in the nav bar |
| Remove a favorite | Click the ♥ button again on a favorited movie |

## API Reference

The app uses two TMDB endpoints:

```
GET /movie/popular        → Trending movies
GET /search/movie?query=  → Search by title
```

Movie posters are served from `https://image.tmdb.org/t/p/w500`.

## License

MIT
