# NewsHub

A React-based news browsing application that fetches and displays the latest top headlines using the NewsAPI. It offers category-based filtering, infinite scrolling for seamless reading, and a smooth user experience with a responsive interface.

## Features

- Category Filtering: Browse news across multiple categories including Business, Entertainment, Health, Science, Sports, and Technology.
- Infinite Scrolling: Automatically loads more articles as you scroll down the page.
- Progress Indication: Features a top loading bar to show network request progress.
- Real-time News: Integrates directly with NewsAPI to fetch the absolute latest headlines.

## Tech Stack

- Frontend: React, React Router
- UI Components: Bootstrap (for layout), React Infinite Scroll Component
- User Experience: React Top Loading Bar
- Data Fetching: Fetch API

## Architecture and Data Flow

1. Initialization: On component mount, the frontend requests news data for the selected category via the NewsAPI.
2. Routing: React Router dynamically renders the `News` component based on category paths (e.g., `/sports`, `/technology`) and passes down the required props.
3. Loading State: The application displays a spinner and updates a top loading bar while waiting for the API response.
4. Data Ingestion: The backend JSON payload is received, parsed, and stored into the local React state.
5. Infinite Scrolling: When the user scrolls near the bottom of the page, the infinite scroll listener triggers a pagination fetch to append new articles to the state.
6. Display: `NewsItem` child components render the individual title, description, author, source, date, and image.

## Getting Started

### Prerequisites

- Node.js and npm
- A free API key from [NewsAPI.org](https://newsapi.org/)

### Setup

```bash
npm install
echo "REACT_APP_NEWS_API=your_news_api_key_here" > .env.local
npm start
```
