# Movie App

A React movie discovery application powered by **The Movie Database (TMDB) API** with **Firebase Authentication**. Users can browse movies, search after signing in, open protected movie detail pages and watch available trailers.

## Live demo

https://movie-app-omersb.vercel.app/

## Features

- Browse featured movies from TMDB
- Search movies by title
- Firebase email/password registration
- Firebase email/password login
- Google sign-in
- Authentication-aware navigation
- Protected movie detail routes
- Movie overview, release date, rating and vote count
- Trailer playback when a TMDB video is available
- Toast notifications for authentication and validation feedback
- Responsive UI with Bootstrap

## Tech stack

- React 18
- React Router
- Axios
- Firebase Authentication
- TMDB API
- Bootstrap
- React Toastify

## Routes

| Route | Purpose |
| --- | --- |
| `/` | Featured movies and search |
| `/login` | User login |
| `/register` | User registration |
| `/details/:id` | Protected movie detail page |

## Environment variables

Create a local `.env` file using the provided `.env.example` template:

```env
REACT_APP_TMDB_KEY=
REACT_APP_apiKey=
REACT_APP_authDomain=
REACT_APP_projectId=
REACT_APP_storageBucket=
REACT_APP_messagingSenderId=
REACT_APP_appId=
```

The TMDB key comes from your TMDB developer account. The Firebase values come from your Firebase web app configuration.

> Never commit your real `.env` file or API credentials.

## Local setup

### 1. Clone the repository

```bash
git clone https://github.com/omersb/Movie_App.git
cd Movie_App
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Copy the example file and add your own credentials:

```bash
cp .env.example .env
```

### 4. Start the development server

```bash
npm start
```

The app will be available at:

```text
http://localhost:3000/
```

## Authentication flow

The app uses Firebase Authentication for:

- account registration
- email/password sign-in
- Google sign-in
- sign-out
- observing the current authenticated user

Movie detail pages are protected and redirect unauthenticated users to the login page.

## TMDB integration

The application uses TMDB endpoints for:

- featured/discover movies
- movie search
- movie details
- movie videos/trailers

## Preview

![Movie App](movie-app.gif)

## Security note

Environment files are intentionally excluded from version control. If credentials were ever committed in an earlier revision, rotate them in the corresponding provider dashboard.

## Author

**Ömer Said Bulduk**

- Portfolio: https://omersb.dev/
- GitHub: https://github.com/omersb
- LinkedIn: https://www.linkedin.com/in/omersaidbulduk/
