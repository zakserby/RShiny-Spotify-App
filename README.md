# RShiny Spotify App

R Shiny app for exploring Spotify's Top Hits of the 2000s playlist, written with Illya Vu for STA 230 (Grinnell College).

Play the app in your browser: https://zakserby.github.io/RShiny-Spotify-App/ (it runs R in the browser with shinylive, so the first load takes about a minute).

Files:

- RShinyApp.R : full app code (data cleaning, UI and server), copied from the R Markdown file
- RShinyApp.pdf : knitted R Markdown file as a PDF, showing the code and its console output
- RShinyApp.html : original knitted R Markdown file (download and open in a browser to view)
- app/app.R : copy of RShinyApp.R used for the web version; the only change is that read_csv reads song_normalize.csv from this folder
- app/song_normalize.csv : song data read by the app
- .github/workflows/deploy-app.yml : builds the web version with shinylive and publishes it to GitHub Pages

App tabs:

- Top Hits 2000s Overview : bar chart of songs by genre or explicitness, filtered by year and artist (barchart), with the number of songs per chosen artist (song2) and a table ranking songs by popularity (poptable)
- Top Hits 2000 Trend : plotly scatter plot of popularity against tempo, duration, loudness or energy with a fitted regression line, filtered by year and artist (scatterplot, song)
- Top Hits 2000 Explorer : plotly scatter plot and data table of songs filtered by danceability, speechiness, instrumentalness and liveness (explot, table)
- About : describes the playlist and defines each musical trait

Data:

- app/song_normalize.csv : 2,000 songs, 18 columns, from the Kaggle dataset "Top Hits Spotify from 2000-2019" (Mark Koverha)

To run locally: install shiny, ggplot2, tidyr, dplyr, plotly, shinythemes, DT, viridis and readr, then run shiny::runApp("app") from the repository folder.
