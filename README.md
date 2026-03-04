# Hallmark Movie Dataset (2010–2025)

A curated dataset of Hallmark movies from 2010 to 2025, built using the [TMDB API](https://developer.themoviedb.org/docs/getting-started) and cross-referenced with IMDB, Hallmark Channel listings, and fan sources.

## Repository Contents

| File | Description |
|------|-------------|
| `Hallmark_Movies_Filtered_2010_2025.csv` | Cleaned, filtered dataset of Hallmark movies (2010–2025) |
| `Creating_Hallmark_Dataset.ipynb` | Notebook for pulling and assembling the dataset via the TMDB API |
| `Exploring Hallmark Dataset.ipynb` | Notebook for descriptive statistics and visualizations |

## Dataset

**`Hallmark_Movies_Filtered_2010_2025.csv`** contains Hallmark movies from 2010–2025, sourced from TMDB and supplemented with IMDB ratings data. The dataset covers movies from Hallmark Media and its partner production companies.

## Notebooks

### Creating_Hallmark_Dataset.ipynb
Covers the full data collection process:
- Querying TMDB's discover endpoint across 60+ Hallmark-affiliated production companies
- Cross-referencing IMDB lists and HallmarkChannel.com to fill gaps
- Deduplication and filtering

### Exploring Hallmark Dataset.ipynb
Descriptive analysis including:
- Movie counts by year and production company
- Trend visualizations using seaborn, matplotlib, and plotly

## Setup

### Prerequisites
- Python 3.x
- Jupyter Notebook

### Install dependencies
```bash
pip install requests pandas python-dotenv seaborn matplotlib scipy numpy plotly jupyter-contrib-nbextensions
```

### TMDB API Key
The data collection notebook requires a free TMDB API key.

1. Register at [themoviedb.org](https://www.themoviedb.org/signup) and request an API key
2. Create a `.env` file in the project root:
```
TMDB_API_KEY=your_actual_api_key_here
```

## Data Sources
- [The Movie Database (TMDB)](https://www.themoviedb.org/) — primary movie metadata
- [IMDB](https://www.imdb.com/) — ratings and supplemental title data
- [HallmarkChannel.com](https://www.hallmarkchannel.com/) — spot-checking new releases
