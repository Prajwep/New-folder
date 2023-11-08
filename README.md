1. Import necessary libraries:
   - `requests`: Used to send HTTP GET requests to IMDb.
   - `BeautifulSoup` from the `bs4` library: Used for parsing HTML content.
   - `pandas` as `pd`: Used for working with data in a tabular format.

2. Define a function `get_top_movies_by_genre(genre)` that takes a genre as input and retrieves the top 5 movies of that genre from IMDb.

3. Inside the `get_top_movies_by_genre` function:
   - Construct the IMDb URL for the specified genre using the `genre` parameter.
   - Send an HTTP GET request to the IMDb URL.
   - Check if the response status code is 200 (indicating a successful request).
   - If the request is successful, parse the HTML content of the page using BeautifulSoup.
   - Find all the movie containers on the page, identified by the class "lister-item-content."
   - Iterate through these containers, extracting the titles of the top 5 movies.
   - Store the movie titles in a list and return it.

4. Outside the function:
   - Prompt the user to input a genre using `input`.
   - Call the `get_top_movies_by_genre` function with the user's chosen genre.
   - If there are top-rated movies for the specified genre:
     - Create a Pandas DataFrame with the movie titles and name the column "Top Movies."
     - Display the top 5 movies of the specified genre in the DataFrame.
   - If no movies are found for the genre, display a corresponding message.

