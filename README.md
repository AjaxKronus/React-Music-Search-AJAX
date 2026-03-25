# BeatStream: iTunes Music Explorer

**BeatStream** is a dynamic React web application that allows users to search, discover, and preview music using the iTunes Search API. By leveraging asynchronous data fetching (AJAX) and modern React hooks, the app delivers a seamless experience for exploring artist discographies and listening to track previews in real time.

-----

## Key Features

  * **Live Album Search:** Instantly query the iTunes database for any artist or group with URL-encoded search handling.
  * **Deep-Dive Track Listings:** Click any album to view its full tracklist, powered by dynamic routing and the `useEffect` hook.
  * **Integrated Audio Previews:** Listen to 30-second high-quality audio samples directly within the browser.
  * **Responsive Feedback:** \* **Loading States:** Visual spinners provide immediate feedback during asynchronous data fetching.
      * **Graceful Error Handling:** Robust `.catch()` logic and user-friendly alerts for network issues or "No Results Found" scenarios.
  * **Modern State Management:** Utilizes React state and effect hooks to synchronize the UI with external API responses.

-----

## Visual Overview

*The interface features a dual-view system: a searchable grid of high-resolution album artwork and a detailed track-by-track breakdown for individual collections.*

-----

## Technical Stack

  * **Frontend:** React.js (JSX)
  * **Data Fetching:** Fetch API with Promises and `whatwg-fetch` polyfill for cross-browser compatibility.
  * **Routing:** React Router (for collection-specific track views).
  * **API:** iTunes Search API (RESTful).
  * **Styling:** Responsive CSS with integrated loading indicators.

-----

## Architecture & Logic

The application is built on a modular component hierarchy:

  * **`App`**: Manages the global state for album results and search status.
  * **`AlbumSearchForm`**: Handles user input, string sanitization, and submission triggers.
  * **`TrackList`**: A specialized view that fetches and parses album-specific data, including logic to filter out non-track metadata from API results.
  * **`AudioPlayer`**: Bridges the iTunes preview URLs to the browser's native audio capabilities.

-----

## Installation & Setup

To run **BeatStream** on your local machine, ensure you have [Node.js](https://nodejs.org/) installed:

1.  **Clone the repository** and enter the project directory:

    ```bash
    cd beatstream-music-search
    ```

2.  **Install the necessary dependencies**:

    ```bash
    npm install
    ```

3.  **Launch the development server**:

    ```bash
    npm start
    ```

4.  **Explore**: The application will open at `http://localhost:3000`.

-----

## Data Disclosure

This project interfaces with the **iTunes Store Web Service**. Search results, album artwork, and audio samples are provided courtesy of Apple Inc. Please note that the API may occasionally return empty results for specific queries due to server-side rate-limiting or availability.
