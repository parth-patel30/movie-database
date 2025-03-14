# movie-database
# 🎬 Movie Database  

**Live Demo:** [Movie Database](https://parth-patel30.github.io/movie-database/)  

---

## 📌 About the Project  
This is a simple **Movie Database** web application that fetches and displays movie details using [TheMovieDB API](https://www.themoviedb.org/). Users can search for movies, view details like ratings, release dates, and descriptions.  

---

## 🚀 Features  
- ✅ Fetches real-time movie data from **TheMovieDB API**  
- ✅ Search movies by name  
- ✅ Displays movie title, release date, and overview  
- ✅ Responsive design for mobile and desktop  
- ✅ Built with **HTML, CSS, and JavaScript**  

---

## 🛠️ Tech Stack  
- **HTML5** → Structure  
- **CSS3** → Styling  
- **JavaScript (ES6)** → Fetch API, DOM Manipulation  
- **TheMovieDB API** → Movie Data  

---

## 🔧 Setup & Installation  

1. **Clone the repository:**  
   ```bash
   git clone https://github.com/parth-patel30/movie-database.git
   cd movie-database
2️. **Open the Website**
Open the index.html file in your browser (Chrome, Firefox, Edge, etc.):

---

🌐 API Setup
Get a free API key from TheMovieDB.
Replace YOUR_API_KEY in the JavaScript file:
```bash
const API_KEY = 'YOUR_API_KEY';
const API_URL = `https://api.themoviedb.org/3/search/movie?api_key=${API_KEY}&query=`;
```
---

📝 Code Overview
🔹 Fetch Movie Data
The app fetches movie data from TheMovieDB API based on the user’s search input:
```bash
async function getMovies(query) {
    const response = await fetch(`${API_URL}${query}`);
    const data = await response.json();
    displayMovies(data.results);
}
```
🔹 Display Movies
The fetched data is processed and displayed dynamically on the page:
```bash
function displayMovies(movies) {
    const movieContainer = document.getElementById("movies");
    movieContainer.innerHTML = ""; // Clear previous results

    movies.forEach(movie => {
        const movieElement = document.createElement("div");
        movieElement.classList.add("movie");
        movieElement.innerHTML = `
            <h2>${movie.title}</h2>
            <p>📅 Release Date: ${movie.release_date}</p>
            <p>⭐ Rating: ${movie.vote_average}</p>
            <p>${movie.overview}</p>
        `;
        movieContainer.appendChild(movieElement);
    });
}
```

---

🎉 Live Preview
The project is hosted on GitHub Pages:

🔗 [Check it live here](https://parth-patel30.github.io/movie-database/) 



