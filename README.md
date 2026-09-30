# RShiny Spotify App

R Shiny app for exploring Spotify's Top Hits of the 2000s playlist by genre, artist, year and musical traits, written with Illya Vu for STA 230 (Grinnell College).

Files:
- RShinyApp.html : knitted R Markdown file with the full app code. It cleans the song data (splits and pivots the genre column, relabels explicit songs), builds a four-tab UI with shinytheme "yeti" (Top Hits 2000s Overview, Top Hits 2000 Trend, Top Hits 2000 Explorer, About) and defines the server: a ggplot2 bar chart of songs by genre or explicitness filtered by year and artist, a DT table ranking songs by popularity, a plotly scatter plot of popularity against tempo, duration, loudness or energy with a fitted regression line, and a plotly explorer filtered by danceability, speechiness, instrumentalness and liveness with a matching data table.

Data:
- The code reads song_normalize.csv (2,000 songs, 18 columns), which is not included in this repository.

To run: copy the code into R with shiny, ggplot2, tidyr, dplyr, plotly, shinythemes, tools, DT, viridis and readr installed, point read_csv to song_normalize.csv and run shinyApp(ui, server). The app does not run inside the static HTML file.
