# Data Analyst Intern Assignment Documentation

## 1. Objective
The goal of this assignment was to analyze user, cooking session, and order data to derive meaningful insights and visualize trends that could help the organization make informed decisions.

---

## 2. Steps Followed

### a. Data Loading
- Imported the datasets `UserDetails.csv`, `CookingSessions.csv`, and `OrderDetails.csv` using the Pandas library.
- Ensured proper handling of encodings and column names.

### b. Data Cleaning
- **User Details:**
  - Filled missing `Age` values with the mean age.
  - Replaced missing `Gender` values with "Unknown."
- **Cooking Sessions:**
  - Dropped rows where `DishPrepared` was missing, as these entries added no value to the analysis.
- **Order Details:**
  - Removed rows with missing `DishOrdered` values to ensure accuracy in insights.

### c. Data Merging
- Merged the datasets using `UserID` as the primary key:
  - `UserDetails` with `CookingSessions` (left join).
  - Resulting data with `OrderDetails` (left join).
- This created a consolidated dataset containing user demographics, cooking activity, and ordering behavior.

### d. Data Analysis
- **Popular Dishes Ordered:**
  - Calculated the frequency of each dish in the `DishOrdered` column.
  - Identified trends in customer preferences.
- **Session and Order Analysis:**
  - Grouped data by `UserID` to count the number of `DishPrepared` and `DishOrdered` entries for each user.
  - Analyzed correlations between cooking sessions and ordering behavior.

### e. Visualization
- Created a bar chart showcasing the most popular dishes ordered:
  - Used `matplotlib` for clear, customizable visualization.
  - Adjusted chart aesthetics (title, labels, and rotation) for readability.

---

## 3. Methodology
- **Data Cleaning:** Ensured the datasets were free of inconsistencies or missing values that could skew results.
- **Exploratory Data Analysis (EDA):** Leveraged statistical methods to examine distributions and trends.
- **Data Integration:** Combined datasets to enable cross-functional analysis of user behavior.
- **Visualization:** Used visual aids to communicate insights effectively.

---

## 4. Key Findings
- **Popular Dishes:**
  - The most frequently ordered dishes were identified, highlighting user preferences.  
- **User Engagement:**
  - Users with more cooking sessions exhibited higher order counts, suggesting a correlation between cooking activity and ordering behavior.  
- **Demographic Insights:**
  - Gender and age distributions provided a deeper understanding of the user base.

---

## 5. Challenges and Solutions
- **Handling Missing Data:**
  - Imputed or removed missing values depending on the column's significance.
- **Data Integration:**
  - Ensured primary keys (`UserID`) matched across datasets to avoid merging errors.

---

## 6. Future Recommendations
- Collect more detailed session and order feedback to refine insights.
- Use advanced statistical models to predict future trends in user ordering and cooking behavior.

---

This documentation, along with the code and visualizations, is available in the provided GitHub repository.
