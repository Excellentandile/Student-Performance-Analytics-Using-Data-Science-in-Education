# Data/Tech Sourcing & Description

## Dataset Description

The project utilizes the **Student Performance Data Set** from the UCI Machine Learning Repository. This dataset comprises information collected from two secondary schools in Portugal, focusing on student achievement in two distinct subjects: Mathematics and Portuguese language. The data was gathered using school reports and questionnaires.

### Source

*   **Origin:** UCI Machine Learning Repository
*   **Donated by:** Paulo Cortez and A. M. G. Silva
*   **Original Paper:** "Using data mining to predict secondary school student performance" by P. Cortez, A. M. G. Silva. 2008. Published in Proceedings of 5th Annual Future Business Technology Conference.
*   **Direct Link:** [https://archive.ics.uci.edu/dataset/320/student+performance](https://archive.ics.uci.edu/dataset/320/student+performance)

### Features

The dataset is multivariate and contains 33 attributes (30 features + 3 grade attributes) for 649 instances (students). It is provided in two separate CSV files:
*   `student-mat.csv`: Data for Mathematics course students.
*   `student-por.csv`: Data for Portuguese language course students.

Both datasets share the same set of attributes, which can be broadly categorized as:

**1. Demographic Information:**
*   `school`: Student's school (binary: 'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira)
*   `sex`: Student's sex (binary: 'F' - female or 'M' - male)
*   `age`: Student's age (numeric: from 15 to 22)
*   `address`: Student's home address type (binary: 'U' - urban or 'R' - rural)
*   `famsize`: Family size (binary: 'LE3' - less or equal to 3 or 'GT3' - greater than 3)
*   `Pstatus`: Parent's cohabitation status (binary: 'T' - living together or 'A' - apart)

**2. Socio-economic and Family-related Factors:**
*   `Medu`: Mother's education (numeric: 0 - none, 1 - primary education (4th grade), 2 - 5th to 9th grade, 3 - secondary education or 4 - higher education)
*   `Fedu`: Father's education (numeric: 0 - none, 1 - primary education (4th grade), 2 - 5th to 9th grade, 3 - secondary education or 4 - higher education)
*   `Mjob`: Mother's job (nominal: 'teacher', 'health' care related, civil 'services', 'at_home' or 'other')
*   `Fjob`: Father's job (nominal: 'teacher', 'health' care related, civil 'services', 'at_home' or 'other')
*   `reason`: Reason to choose this school (nominal: close to 'home', school 'reputation', 'course' preference or 'other')
*   `guardian`: Student's guardian (nominal: 'mother', 'father' or 'other')
*   `famrel`: Quality of family relationships (numeric: from 1 - very bad to 5 - excellent)
*   `freetime`: Free time after school (numeric: from 1 - very low to 5 - very high)
*   `goout`: Going out with friends (numeric: from 1 - very low to 5 - very high)
*   `Dalc`: Workday alcohol consumption (numeric: from 1 - very low to 5 - very high)
*   `Walc`: Weekend alcohol consumption (numeric: from 1 - very low to 5 - very high)
*   `health`: Current health status (numeric: from 1 - very bad to 5 - very good)

**3. School-related and Academic Factors:**
*   `traveltime`: Home to school travel time (numeric: 1 - <15 min., 2 - 15 to 30 min., 3 - 30 min. to 1 hour, or 4 - >1 hour)
*   `studytime`: Weekly study time (numeric: 1 - <2 hours, 2 - 2 to 5 hours, 3 - 5 to 10 hours, or 4 - >10 hours)
*   `failures`: Number of past class failures (numeric: n if 1<=n<3, else 4)
*   `schoolsup`: Extra educational support (binary: yes or no)
*   `famsup`: Family educational support (binary: yes or no)
*   `paid`: Extra paid classes within the course subject (binary: yes or no)
*   `activities`: Extra-curricular activities (binary: yes or no)
*   `nursery`: Attended nursery school (binary: yes or no)
*   `higher`: Wants to take higher education (binary: yes or no)
*   `internet`: Internet access at home (binary: yes or no)
*   `romantic`: With a romantic relationship (binary: yes or no)
*   `absences`: Number of school absences (numeric: from 0 to 93)

**4. Target Variables (Grades):**
*   `G1`: First period grade (numeric: from 0 to 20)
*   `G2`: Second period grade (numeric: from 0 to 20)
*   `G3`: Final grade (numeric: from 0 to 20, **output target**)

An important note from the dataset creators is that `G3` has a strong correlation with `G1` and `G2`, as `G3` is the final year grade, and `G1` and `G2` are earlier period grades. Predicting `G3` without `G1` and `G2` is more challenging but also more useful for early intervention.

### Technological Framework

For this project, the primary technological framework will involve:
*   **Programming Language:** Python 3.x
*   **Data Manipulation and Analysis:** Pandas, NumPy
*   **Data Visualization:** Matplotlib, Seaborn
*   **Machine Learning:** Scikit-learn (for model building, evaluation, and statistical tests)
*   **Reporting:** Markdown for documentation and potentially Jupyter Notebooks for interactive analysis.
