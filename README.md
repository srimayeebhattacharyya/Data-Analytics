# Netflix Movie Data Analysis Dashboard
Interactive Netflix-style content analysis dashboard using **Google Sheets** with pivot insights and investment vs return views.

---

## 1. Project Title
**Netflix Movie Data Analysis Using Google Sheets**

---

## 2. Project Overview

This project analyzes a Netflix-style content catalog to uncover insights on content distribution, financial performance, and audience-related indicators.

The workflow starts from raw data and proceeds through cleaning, pivot-table analysis, and dashboard visualization. The final output provides a compact analytical view that can support exploratory reporting and business-oriented content decisions.

### Key Objectives

- Analyze content mix across Movies, TV Series, Documentaries, and related formats
- Compare production investment against box office returns
- Evaluate average duration and IMDb rating by content type
- Assess country-level contribution to investment and returns
- Build a dashboard-ready Excel analysis layer from the raw dataset

---

## 3. Project Structure

| Folder | File | Description |
|---|---|---|
| Raw Dataset | `Raw Dataset/Movies.csv` | Original source dataset |
| Clean Dataset | `Clean Dataset/Clean movies.xlsx` | Cleaned workbook with analysis sheets |
| Clean Dataset | `Clean Dataset/Clean movies - movies.pdf` | PDF export of cleaned sheet |
| Pivot Tables and Calculations | `Pivot Tables and Calculations/Movies Pivot Data Analysis1.xlsx` | Pivot analysis workbook (v1) |
| Pivot Tables and Calculations | `Pivot Tables and Calculations/Movies Pivot Data Analysis2.xlsx` | Pivot analysis workbook (v2) |
| Dashboard | `Dashboard/Screenshot 2026-02-24 011043.png` | Dashboard screenshot |

---

## 4. Data Dictionary

| Column Name | Data Type | Description |
|---|---|---|
| `movie_id` | Text | Unique identifier in `movie_####` format |
| `title` | Text | Name of the movie/content title |
| `content_type` | Text | Content category (Movie, TV Series, Documentary, etc.) |
| `genre_primary` | Text | Primary genre |
| `genre_secondary` | Text | Secondary genre |
| `release_year` | Integer | Release year |
| `duration_minutes` | Integer | Runtime in minutes |
| `rating` | Text | Content certification rating |
| `language` | Text | Primary language |
| `country_of_origin` | Text | Country of production |
| `imdb_rating` | Decimal | IMDb score (0-10) |
| `production_budget` | Decimal | Production budget |
| `box_office_revenue` | Decimal | Box office revenue |
| `number_of_seasons` | Integer | Number of seasons (series content) |
| `number_of_episodes` | Integer | Number of episodes (series content) |
| `is_netflix_original` | Boolean | Netflix Original flag (`TRUE/FALSE`) |
| `added_to_platform` | Date | Date added to platform |
| `content_warning` | Boolean | Content warning flag (`TRUE/FALSE`) |

---

## 5. Data Summary

- Total records: **1,040**
- Total columns: **18**
- Missing values: **0** (all columns complete)
- Release year range: **1953-2024**
- Added to platform range: **2020-08-02 to 2025-08-01**
- IMDb rating (min-max-avg): **0.5 - 10.0 - 6.273**
- Netflix Originals: **318 (30.58%)**
- Content warning flagged: **201 (19.33%)**
- Total production budget: **11,560,030,704**
- Total box office revenue: **67,195,370,225.19**
- Revenue-to-budget ratio: **5.813x**

### Content Type Distribution

- Movie: **458 (44.04%)**
- TV Series: **267 (25.67%)**
- Documentary: **142 (13.65%)**
- Stand-up Comedy: **119 (11.44%)**
- Limited Series: **54 (5.19%)**

### Top Languages

- English: **608**
- Spanish: **103**
- French: **67**
- Hindi: **60**
- Japanese: **55**

### Top Countries

- USA: **543**
- South Korea: **118**
- Canada: **102**
- UK: **88**
- Japan: **57**

---

## 6. Cleaning Notes

The cleaned workbook (`Clean movies.xlsx`) uses a slightly transformed structure:

- `movie_id` is split into `movie` and `id` columns
- `title` is not retained in the cleaned sheet
- Date values are stored in Excel serial format internally

Additional quality checks observed on raw data:

- `movie_id` duplicates found: **40** IDs (each repeated twice)
- `title` duplicates found: **262** values (expected for reused/franchise naming)
- Series metrics (`number_of_seasons`, `number_of_episodes`) are zero for most non-series records

---

## 7. Analytics View

The pivot analysis workbooks include:

### Pivot Table 3 (by `content_type`)

- Count of IDs
- Average duration
- Average IMDb rating
- Sum of production budget
- Sum of box office revenue
- Sum of seasons
- Sum of episodes

### Pivot Table 6 (by `country_of_origin`)

- Count of IDs
- Sum of production budget
- Sum of box office revenue

Dashboard visuals include:

- Content type wise content count
- Content type wise duration comparison
- Average IMDb rating by content type
- Investment vs return analysis
- Country-wise investment vs return comparison

---

## 8. Tools Used

- **Microsoft Excel**
- Pivot Tables
- Pivot Charts
- Dashboard layout and KPI cards

---

## 9. Dashboard Image

![Dashboard](Dashboard/Screenshot%202026-02-24%20011043.png)

---

## 10. Conclusion

This project demonstrates a complete Excel-based analytics pipeline from raw data to dashboard delivery.

Key takeaways:

- Movies represent the largest content share and largest financial contribution
- Box office return is substantially higher than production investment at portfolio level
- USA dominates both investment and revenue among origin countries
- Rating and duration comparisons across content types provide useful segmentation signals

Overall, the dashboard provides a practical foundation for content strategy review and further advanced analytics.

---

## 11. Future Enhancements

1. Add monthly/yearly trend analysis using `added_to_platform`
2. Create Originals vs Non-Originals comparative dashboard page
3. Build a separate data dictionary file with business definitions and units
4. Introduce validation rules for unique ID integrity and duplicate tracking
