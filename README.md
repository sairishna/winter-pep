[2:07 pm, 5/2/2025] +91 63015 24134: # Assignment

### *Assignment: Movie Catalog*

You have been hired to build a *Movie Catalog* that manages a collection of movies. Each movie has several properties, including its title, release year, genre, and rating. Your task is to perform various operations on the movie catalog.

### *Movie Data Format:*

The movie data is an array of objects, where each object represents a movie. Each movie object will have the following properties:

- title: The title of the movie (string).
- releaseYear: The year the movie was released (number).
- genre: The genre of the movie (string).
- rating: The movie's rating (number, between 1 and 10).

js
const movies = [
  { title: 'Inception', releaseYear: 2010, genre: 'Sci-Fi', rating: 8.8 },
  { title: 'The Dark Knight', releaseYear: 2008, genre: 'Action', rating: 9.0 },
  { title: 'Titanic', releaseYear: 1997, genre: 'Romance', rating: 7.8 },
  { title: 'The Matrix', releaseYear: 1999, genre: 'Sci-Fi', rating: 8.7 },
  { title: 'The Godfather', releaseYear: 1972, genre: 'Crime', rating: 9.2 },
  { title: 'Avatar', releaseYear: 2009, genre: 'Sci-Fi', rating: 7.8 },
  { title: 'The Shawshank Redemption', releaseYear: 1994, genre: 'Drama', rating: 9.3 }
];



You can add more values to the array

### Tasks:

1. *Sort the Movies by Rating*: Sort the movies so that the highest-rated movie comes first.
2. *Find a Movie by Title*: Write a function that takes a movie title as a parameter and returns the movie object. If no movie is found, return a message indicating that the movie is not in the catalog.
3. *Get Movies with a Rating Greater Than 8*: Create a new array of movies that have a rating greater than 8.
4. *List All Movie Titles*: Create an array of only the movie titles.
5. *Count Movies in a Specific Genre*: Write a function that takes a genre as a parameter and returns the number of movies in that genre.
6. *Check if All Movies Are Rated Above 7*: Check if every movie in the catalog has a rating above 7.
7. *Get Movies Released After 2000*: Create a new array that includes only movies released after the year 2000.
[2:07 pm, 5/2/2025] +91 63015 24134: const movies = [
    { title: 'Inception', releaseYear: 2010, genre: 'Sci-Fi', rating: 8.8 },
    { title: 'The Dark Knight', releaseYear: 2008, genre: 'Action', rating: 9.0 },
    { title: 'Titanic', releaseYear: 1997, genre: 'Romance', rating: 7.8 },
    { title: 'The Matrix', releaseYear: 1999, genre: 'Sci-Fi', rating: 8.7 },
    { title: 'The Godfather', releaseYear: 1972, genre: 'Crime', rating: 9.2 },
    { title: 'Avatar', releaseYear: 2009, genre: 'Sci-Fi', rating: 7.8 },
    { title: 'The Shawshank Redemption', releaseYear: 1994, genre: 'Drama', rating: 9.3 }
  ];
  
  // 1. Sort the Movies by Rating (Highest First)
  const sortedByRating = [...movies].sort((a, b) => b.rating - a.rating);
  console.log("Sorted by Rating:", sortedByRating);
  
  // 2. Find a Movie by Title
  const findMovieByTitle = (title) => {
    const movie = movies.find(movie => movie.title.toLowerCase() === title.toLowerCase());
    return movie ? movie : Movie with title "${title}" not found.;
  };
  console.log(findMovieByTitle("Titanic"));
  
  // 3. Get Movies with a Rating Greater Than 8
  const highRatedMovies = movies.filter(movie => movie.rating > 8);
  console.log("Movies with rating greater than 8:", highRatedMovies);
  
  // 4. List All Movie Titles
  const movieTitles = movies.map(movie => movie.title);
  console.log("Movie Titles:", movieTitles);
  
  // 5. Count Movies in a Specific Genre
  const countMoviesByGenre = (genre) => {
    return movies.filter(movie => movie.genre.toLowerCase() === genre.toLowerCase()).length;
  };
  console.log("Number of Sci-Fi movies:", countMoviesByGenre("Sci-Fi"));
  
  // 6. Check if All Movies Are Rated Above 7
  const allAboveSeven = movies.every(movie => movie.rating > 7);
  console.log("Are all movies rated above 7?", allAboveSeven);
  
  // 7. Get Movies Released After 2000
  const moviesAfter2000 = movies.filter(movie => movie.releaseYear > 2000);
  console.log("Movies released after 2000:", moviesAfter2000);
