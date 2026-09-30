# RShiny Spotify App

R Shiny app for exploring Spotify's Top Hits of the 2000s playlist, written with Illya Vu for STA 230 (Grinnell College).

Files:

- RShinyApp.html : knitted R Markdown file containing the full app code (data cleaning, UI and server)

Data cleaning:

- separate splits the genre column into each song's two most prominent genres
- pivot_longer reshapes the data to one row per song and genre, dropping missing genres
- toTitleCase and relabeling tidy the genre and explicit columns and rename duration_ms to duration

App tabs:

- Top Hits 2000s Overview : bar chart of songs by genre or explicitness, filtered by year and artist (barchart), with the number of songs per chosen artist (song2) and a table ranking songs by popularity (poptable)
- Top Hits 2000 Trend : plotly scatter plot of popularity against tempo, duration, loudness or energy with a fitted regression line, filtered by year and artist (scatterplot, song)
- Top Hits 2000 Explorer : plotly scatter plot and data table of songs filtered by danceability, speechiness, instrumentalness and liveness (explot, table)
- About : describes the playlist and defines each musical trait

Data:

- song_normalize.csv (2,000 songs, 18 columns) is read by the code and is not included in this repository.

To run: copy the code into R with shiny, ggplot2, tidyr, dplyr, plotly, shinythemes, tools, DT, viridis and readr installed, point read_csv to song_normalize.csv and run shinyApp(ui, server). The app does not run inside the static HTML file.
