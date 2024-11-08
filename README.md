# mainflow task 2  
### YouTube Trending Videos Analysis - Exploratory Data Analysis (EDA)
## Project Overview
This project focuses on performing **Exploratory Data Analysis (EDA)** on a dataset of trending YouTube videos. The objective is to extract valuable insights, detect patterns, and understand the relationships between different features affecting video popularity. By leveraging Python and its powerful data analysis libraries, we aim to uncover key trends in user engagement metrics like views, likes, and comments.

## Dataset Description
The dataset used in this project is **`INDIAvi.csv`**, which consists of information about trending YouTube videos. Here is an overview of some key columns:

| Column                  | Description                                         |
|-------------------------|-----------------------------------------------------|
| `video_id`              | Unique identifier for the video                    |
| `title`                 | Title of the video                                 |
| `channel_title`         | Name of the YouTube channel                        |
| `category_id`           | ID representing the video category                 |
| `views`                 | Number of views on the video                       |
| `likes`                 | Number of likes on the video                       |
| `dislikes`              | Number of dislikes on the video                    |
| `comment_count`         | Number of comments on the video                    |
| `comments_disabled`     | Boolean indicating if comments are disabled        |
| `ratings_disabled`      | Boolean indicating if ratings are disabled         |
| `video_error_or_removed`| Boolean indicating if the video was removed        |

### Goals of Analysis
- **Generate summary statistics** to understand the data distribution.
- **Detect outliers** using statistical methods like IQR (Interquartile Range).

## Methodology
The project follows a structured EDA process:

### 1. **Data Loading and Preprocessing**
   - Imported the dataset using `pandas`.

### 2. **Summary Statistics and Missing Values Check**
   - Used `.describe()` to generate summary statistics for numerical features.
   - Identified missing values and handled them appropriately.

### 3. **Quantile Analysis and Outlier Detection**
   - Calculated the **Interquartile Range (IQR)** to detect outliers in key numerical columns like `views`, `likes`, `dislikes`, and `comment_count`.
   - Defined the lower and upper bounds to identify potential outliers using:
     ```math
     Lower Bound = Q1 - 1.5 * IQR
     ```
      ```math
     Upper Bound = Q3 + 1.5 * IQR
     ```
   - Filtered out outlier rows and analyzed their impact on the dataset.

## Tools and Libraries Used
- **Python**: The primary programming language.
- **Libraries**:
  - `pandas` - Data manipulation and analysis.
  - `numpy` - Numerical operations and calculations.
  - `scipy` - Statistical analysis and hypothesis testing.

## Initial Insights
- Outlier detection using quantile analysis revealed that features like `views` and `likes` have a significant number of outliers, indicating viral content or anomalies.
- Boolean features such as `comments_disabled` and `ratings_disabled` will be analyzed further to understand their impact on video engagement.

## Next Steps
- Complete data visualization for deeper insights.
- Conduct hypothesis testing to validate relationships between features.
- Explore potential machine learning applications for predicting video popularity based on initial EDA findings.
