# 🎬 Movie Explorer App

A modern movie discovery web app built using **React (Vite)**, powered by the **TMDB API**, with **Appwrite backend integration** for tracking trending searches.

---

## 🚀 Live Demo: 
https://movie-site-react-chinmayee-sbs-projects.vercel.app/

---

##  Features

* Search for movies in real-time
* Discover popular movies (default view)
* Debounced search for optimized API calls
* Tracks trending searches using Appwrite database
* Modern UI built with Tailwind CSS
* Loading spinner & error handling
* Responsive design

---

## 🧠 Tech Stack

* **Frontend:** React (Vite)
* **Styling:** Tailwind CSS
* **API:** TMDB (The Movie Database)
* **Backend (BaaS):** Appwrite
* **Deployment:** Vercel

---

## Project Structure

```
src/
│── components/
│   ├── Search.jsx
│   ├── MovieCard.jsx
│   ├── Spinner.jsx
│
│── App.jsx
│── main.jsx
│── appwrite.js
│── index.css
```

---

## Environment Variables

Create a `.env` file in the root:

```
VITE_TMDB_API_KEY=your_tmdb_token
VITE_APPWRITE_PROJECT_ID=your_project_id
VITE_APPWRITE_DATABASE_ID=your_database_id
VITE_APPWRITE_TABLE_ID=your_table_id
VITE_APPWRITE_ENDPOINT=https://cloud.appwrite.io/v1
```

⚠️ Never commit `.env` to GitHub

---

## API Usage

* **Discover Movies:**

```
/discover/movie?sort_by=popularity.desc
```

* **Search Movies:**

```
/search/movie?query=<searchTerm>
```

---

## How It Works

### 1. Default Load

* App fetches popular movies using TMDB
* Displays top results

### 2. Search

* User types in search bar
* Input is debounced (500ms)
* API is called only after user stops typing

### 3. Data Tracking (Appwrite)

* Searches are stored in database
* If search exists → increment count
* Else → create new record

---

## Installation

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
npm install
npm run dev
```

---

## Deployment

Deployed using Vercel:

1. Push project to GitHub
2. Import repo in Vercel
3. Add environment variables
4. Deploy

---

## ⚠️ Common Issues

* Case-sensitive imports (important for deployment)
* Missing environment variables
* Appwrite domain not added → CORS issues

---

## 🙌 Acknowledgements

* TMDB API for movie data
* Appwrite for backend services
* Vercel for deployment

---

## Author: 
Chinmayee S. Bharadwaj**

---

## ⭐ If you like this project

Give it a star ⭐ on GitHub!
