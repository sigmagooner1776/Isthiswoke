<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Is This Woke or Not?</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f9;
      color: #333;
    }
    header {
      background-color: #4CAF50;
      color: white;
      text-align: center;
      padding: 20px 0;
    }
    header h1 {
      margin: 0;
    }
    #searchSection {
      margin: 20px auto;
      text-align: center;
    }
    #movieSearch {
      width: 70%;
      padding: 10px;
      font-size: 16px;
    }
    #searchBtn {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #333;
      color: white;
      border: none;
      cursor: pointer;
    }
    #searchBtn:hover {
      background-color: #555;
    }
    main {
      max-width: 800px;
      margin: 20px auto;
      padding: 20px;
      background: white;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    #movieResult img {
      max-width: 100%;
      height: auto;
      display: block;
      margin: 0 auto;
    }
    #ratingResult {
      margin-top: 20px;
      text-align: center;
    }
    .rating-bar {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 10px;
    }
    .rating-bar span {
      font-size: 18px;
      margin-left: 10px;
    }
    footer {
      text-align: center;
      padding: 10px 0;
      background-color: #333;
      color: white;
    }
  </style>
</head>
<body>
  <header>
    <h1>Is This Woke or Not?</h1>
  </header>

  <section id="searchSection">
    <input type="text" id="movieSearch" placeholder="Search for a movie title...">
    <button id="searchBtn">Search</button>
  </section>

  <main>
    <section id="movieResult">
      <h2>Movie Details</h2>
      <p>No movie selected yet. Use the search bar above to find a movie.</p>
    </section>

    <section id="ratingResult">
      <h2>Woke Rating</h2>
      <p>No rating available yet.</p>
    </section>
  </main>

  <footer>
    <p>&copy; 2024 Is This Woke or Not</p>
  </footer>

  <script>
    const searchBtn = document.getElementById('searchBtn');
    const movieResult = document.getElementById('movieResult');
    const ratingResult = document.getElementById('ratingResult');

    searchBtn.addEventListener('click', () => {
      const movieTitle = document.getElementById('movieSearch').value;

      if (movieTitle.trim() === '') {
        alert('Please enter a movie title!');
        return;
      }

      movieResult.innerHTML = `
        <h2>${movieTitle}</h2>
        <img src="https://via.placeholder.com/300x450" alt="${movieTitle}">
        <p>This is a placeholder for the movie details.</p>
      `;

      ratingResult.innerHTML = `
        <h2>Woke Rating</h2>
        <p>This movie scored a 7/10 on the woke scale.</p>
        <div class="rating-bar">
          <div style="width: 70%; height: 20px; background-color: #4CAF50;"></div>
          <span>7/10</span>
        </div>
        <p>Explanation: This movie features diverse representation and explores modern social themes, but balances them with a strong narrative.</p>
      `;
    });
  </script>
</body>
</html>
