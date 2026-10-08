# Verification record

Verified locally on 8 October 2026 with Python 3.12.14.

- All 15 code cells executed sequentially without errors.
- Exactly five embedded PNG chart outputs in the saved notebook.
- Notebook schema validated with nbformat.
- Exactly five chart PNGs, each at 300 DPI; charts visually inspected separately.
- Raw CSV: 32,833 rows, 23 columns; unchanged from source.
- No exact full-row duplicates; missing song names/artists: 5 rows each.
- Unique valid tracks: 28,351; unique track/genre pairs: 30,379.
- Numeric values agree across repeated track IDs before deduplication.
- Artist means independently recalculated using sum / count, with minimum 20 tracks.
- Genre means independently recalculated using sum / count.
- Danceability correlation checked against NumPy corrcoef.
- Actual ZIP extracted to a different directory and every cell re-executed successfully there.
- No GitHub write operations performed.

## Chart dimensions
- `genre_popularity.png`: 2906 × 1709, 300 DPI.
- `top_artists.png`: 3209 × 2009, 300 DPI.
- `song_duration.png`: 2905 × 1709, 300 DPI.
- `danceability_vs_popularity.png`: 2906 × 1709, 300 DPI.
- `correlation_heatmap.png`: 3261 × 2766, 300 DPI.

## Tested analysis library versions
Pandas 3.0.1; NumPy 2.3.5; Matplotlib 3.11.2; Seaborn 0.13.2.

## Independently recalculated findings
- Raw records: 32,833; unique valid tracks: 28,351; unique track/genre pairs: 30,379.
- Highest genre mean: POP, 45.91; lowest: EDM, 34.07.
- Top eligible artist: Billie Eilish, mean 76.96, 26 tracks (minimum 20 distinct tracks).
- Mean duration: 3.78 minutes; median: 3.62; 70.3% last 3–5 minutes inclusive.
- Danceability–popularity Pearson correlation: 0.046.


## Final presentation improvements — 8 October 2026
- Re-executed all 15 code cells successfully; exactly five embedded chart outputs.
- Scatter marker size reduced from 9 to 3 and opacity from 0.20 to 0.10. No sampling: all 28,351 tracks plotted, labelled explicitly. Pearson correlation still uses the full cleaned table.
- Heatmap enlarged from 10 × 8 to 12 × 9.5 inches, with 13-point correlation values and 12-point axis labels.
- Added concise viva explanations for duplicate handling, the 20-track artist threshold, near-zero correlation and historical data.
- Every non-image notebook output compared with the previous version: numeric tables, correlations and computed findings are unchanged.
- SHA-256 checks confirm unchanged dataset, requirements file and the three unaffected chart PNGs.
- All five PNGs checked at 300 DPI; latest scatter and heatmap visually inspected.
- Final ZIP contents checked byte-for-byte against every project file.
- No GitHub operations performed.
