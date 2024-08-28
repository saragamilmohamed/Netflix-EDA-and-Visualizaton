
# Netflix Data Analysis

## Overview
This project involves an in-depth analysis of the Netflix dataset using Python. The dataset contains information about various titles available on Netflix, including movies and TV shows, along with details such as the title, director, cast, country, rating, and duration. The objective of this analysis is to uncover trends, patterns, and insights within the Netflix catalog.

## Dataset
The dataset used in this project is `netflix_titles.csv`, which includes the following columns:
- `show_id`: Unique ID for each show
- `type`: Indicates whether the title is a Movie or a TV Show
- `title`: The title of the movie or TV show
- `director`: Director of the movie or TV show
- `cast`: Cast members
- `country`: Country where the movie or show was produced
- `date_added`: Date when the title was added to Netflix
- `release_year`: Year the title was released
- `rating`: The rating of the title (e.g., PG-13, TV-MA)
- `duration`: Duration of the movie or the number of seasons for TV shows
- `listed_in`: Genres or categories the title belongs to
- `description`: A brief description of the title


1. **Loading and Viewing Data:**
   - The dataset is loaded using pandas, and initial inspections are conducted using `.head()`, `.info()`, and `.describe()` to understand the data structure.

2. **Handling Missing Data:**
   - Missing data in columns like `director`, `cast`, `country`, `date_added`, `rating`, and `duration` were identified.
   - Missing values in `director` and `country` were filled with 'Unknown' and 'other', respectively.
   - The `date_added`, `rating`, and `duration` columns were cleaned by dropping rows with missing values.

3. **Feature Engineering:**
   - Extracted additional features from the `date_added` column: `year_added`, `month_added`, and `day_added`.
   - Mapped the `rating` to target audience ages (e.g., Kids, Teens, Adults).
   - Separated duration data into `season_count` for TV shows and `duration` for movies.

4. **Data Visualization:**
   - **Year Added**: Visualized the number of titles added each year using a count plot.
   - **Movies vs. TV Shows**: A pie chart was created to show the distribution of movies and TV shows.
   - **Country Analysis**: Analyzed the number of titles by country and visualized the top 10 countries producing content for Netflix.
   - **Release Year**: Visualized the distribution of titles by release year.
   - **Director Analysis**: Analyzed and visualized the top 5 directors in the dataset.
   - **Content Listing**: Analyzed the most common genres or categories in the dataset.
   - **Target Age Groups**: Visualized the distribution of target age groups for both movies and TV shows.
   - **Seasonality of Content Added**: Mapped the `month_added` column to seasons (Winter, Spring, Summer, Autumn) and visualized the seasonality of content addition to Netflix.

## Libraries Used
- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `matplotlib`: For creating static, animated, and interactive visualizations.
- `seaborn`: For data visualization based on matplotlib.


## Key Insights
- A large portion of the content on Netflix has been added in recent years, reflecting Netflix's expanding catalog.
- The United States is the top content producer for Netflix, followed by India and other countries.
- Most titles are rated for Adults, reflecting the mature content available on the platform.
- There is a seasonal trend in when content is added, with spikes in certain months, possibly aligning with holiday seasons or strategic releases.

## Conclusion
This project provides a comprehensive analysis of Netflix's catalog, offering insights into the types of content available, the demographics they target, and the trends in content addition. This analysis could be useful for content creators, marketers, or anyone interested in the dynamics of Netflix's offerings.

