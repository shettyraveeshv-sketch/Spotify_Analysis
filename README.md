# Spotify_Analysis
Exploratory data analysis (EDA) in Python of a cleaned Spotify dataset. It covers 8,582 tracks by 2,547 artists across 5,205 albums, released between 1952 and October 2025. The analysis looks at what shapes track popularity and how artists, genres, albums and release years compare.

Dataset (spotify_data_clean)
15 columns, one row per track:

Track: track_id, track_name, track_number, track_popularity, explicit, track_duration_min
Artist: artist_name, artist_popularity, artist_followers, artist_genres
Album: album_id, album_name, album_release_date, album_total_tracks, album_type

Tools: Python, pandas, NumPy, Matplotlib (Jupyter Notebook)

Workflow

Inspection: shape, dtypes, summary statistics, null counts and unique counts.
Cleaning:
Checked for duplicate rows and dropped them.
Converted 'N/A' genres to proper nulls.
Filled 3 missing artist names with “Unknown”.
Parsed release dates into a release_year feature.
Visual analysis:
Distributions: album type and explicit share as pie charts, plus histograms of popularity, duration and album size.
Rankings: top artists by track count, popularity and followers, plus top genres, most popular tracks and longest tracks.
Trends: tracks released per year and average popularity by year (2000 onward).
Relationships: scatter plots (duration, artist popularity and followers against popularity), an explicit vs. non-explicit box plot, and a correlation heatmap.
Album structure: popularity by track position, album size and album type.

Key findings

Albums make up about 68% of tracks, singles 26% and compilations 6%. About 25% of tracks are explicit.
Mean track popularity is about 52 and the median is 58, so the distribution is skewed toward lower values.
Artist popularity is the strongest predictor of track popularity (r ≈ 0.47). Followers (0.23) and duration (0.11) are weaker. Track position and album size have almost no effect (r ≈ −0.03 and −0.05).
Explicit tracks average higher popularity than non-explicit ones (about 57.8 vs. 50.5).
Taylor Swift has the most tracks in the set (324), followed by The Weeknd, Lana Del Rey, Ariana Grande and Nirvana.
About 39% of tracks have no genre data (3,361 of 8,582), which limits the genre analysis.
