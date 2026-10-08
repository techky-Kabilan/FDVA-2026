# Spotify Music Trends Analysis

Beginner-friendly FDVA mini-project for the model examination on **10 October 2026**. Five visualizations explore genre and artist popularity, song durations, danceability and audio-feature correlations. No machine learning, dashboard or API key is required.

## Objectives
Inspect a real CSV, identify missing values and repeated records, prepare clear analysis tables, visualize patterns and explain findings without causal claims.

## Dataset and usage conditions
**Spotify Songs**, published by TidyTuesday on 21 January 2020: 32,833 rows and 23 columns. The original CSV is included unchanged.

- [Source and data dictionary](https://github.com/rfordatascience/tidytuesday/blob/main/data/2020/2020-01-21/readme.md)
- [Direct CSV](https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2020/2020-01-21/spotify_songs.csv)
- Spotify metadata collected with `spotifyr`; TidyTuesday credits Kaylin Pavlik and the package authors.
- [Hosting repository license: CC0 1.0](https://github.com/rfordatascience/tidytuesday/blob/main/LICENSE). No separate dataset-specific license is stated on its dataset page. This does not establish rights over third-party Spotify content. The copied repository license and download checksum are in `data/`.
- Accessed 8 October 2026. These are historical patterns, not 2026 listening trends.

`playlist_genre` is a playlist-derived genre proxy. Genre means use one track per genre; all other charts use one record per track ID. Multi-genre tracks can appear in multiple groups. Artist strings, including collaborations, are kept as supplied. Valid zero popularity and long durations are retained. Missing required fields and invalid numeric values are removed; missing identities are not guessed. See executed cleaning outputs for counts.

## Technologies
Python 3.12 (tested), Jupyter Notebook, Pandas, NumPy, Matplotlib and Seaborn. IPython provides rich notebook interpretations; pathlib provides portable relative paths. Core analysis library versions are pinned in `requirements.txt`.

## How to run
1. Extract the ZIP and open a terminal **inside `Mini_Project_Spotify_Music_Trends_Analysis`**.
2. Create and activate an environment:

   Windows:
   ```powershell
   py -3.12 -m venv .venv
   .venv\Scripts\Activate.ps1
   ```
   macOS / Linux (Python 3.12 installed):
   ```bash
   python3.12 -m venv .venv
   source .venv/bin/activate
   ```
3. Install and start Jupyter:
   ```bash
   python -m pip install -r requirements.txt
   python -m notebook
   ```
4. Open `Mini_Project_Spotify_Music_Trends_Analysis.ipynb`, choose the environment's Python kernel, then use **Restart Kernel and Run All Cells**.

Internet is required for initial package installation only. The notebook reads the included CSV and regenerates the five PNG files using relative paths. The saved notebook already contains executed tables, interpretations and embedded charts for review on GitHub or Jupyter. Open the PNG directly if a notebook renderer uses a small display area.

## Visualizations
The exact Neon Sunset palette is used: background `#1C1228`, coral `#FB7185`, violet `#C084FC`, gold `#FBBF24`, text `#F8FAFC`. All charts export at 300 DPI.

| Chart | Method | File |
|---|---|---|
| Genre popularity | Vertical bars of mean popularity, unique track/genre pairs | `charts/genre_popularity.png` |
| Top artists | Horizontal bars; top 10 eligible artist strings, minimum 20 tracks | `charts/top_artists.png` |
| Song duration | Histogram in minutes, full observed range, mean and median | `charts/song_duration.png` |
| Danceability vs popularity | All 28,351 unique tracks; smaller markers (size 3, opacity 0.10); full-data correlation | `charts/danceability_vs_popularity.png` |
| Audio features | Annotated Pearson correlation heatmap, −1 to +1 | `charts/correlation_heatmap.png` |

## Findings calculated from the supplied CSV
- Raw records: 32,833; unique valid tracks: 28,351; unique track/genre pairs: 30,379.
- Highest genre mean: POP, 45.91; lowest: EDM, 34.07.
- Top eligible artist: Billie Eilish, mean 76.96, 26 tracks (minimum 20 distinct tracks).
- Mean duration: 3.78 minutes; median: 3.62; 70.3% last 3–5 minutes inclusive.
- Danceability–popularity Pearson correlation: 0.046.

The notebook explains every chart and reports the strongest selected correlations. These findings apply to the historical playlist-selected sample. They do not establish worldwide rankings, causal effects or predictive accuracy. The artist threshold is a descriptive choice, not a significance test.

## Verification
Every code cell was executed in order with no errors, five chart images were embedded, exported PNG resolution was checked, and key findings were independently recomputed. The complete ZIP was extracted to a separate folder and re-executed there to verify portable paths. See `VERIFICATION.md` for the tested versions and exact counts.

## Reference and originality
The [supplied FDVA reference notebook](https://github.com/Adeline187/FDVA-2026/blob/main/Mini_Project/Rakshi_FDVA_minipro.ipynb) was inspected for academic organization. This project uses original Spotify calculations and a simpler five-chart structure. No reference code or analysis was copied.

## GitHub status
Published after final project and destination approval in `techky-Kabilan/FDVA-2026`, branch `main`, folder `FDVA/Mini_Project_Spotify_Music_Trends_Analysis/`. Existing coursework is preserved.

[Open the executed mini-project notebook](Mini_Project_Spotify_Music_Trends_Analysis.ipynb).
