# Indian Tech Job Market 2026: Exploratory Data Analysis & Insights

This repository contains an in-depth Exploratory Data Analysis (EDA) of the Indian tech job market in 2026. Using a rich dataset of over **23,000+ job listings**, this analysis explores salary distributions, hiring locations, workplace policies (Remote vs. Hybrid vs. On-site), required experience tiers, and the premium associated with key skills (such as Generative AI, MLOps, and Predictive Modeling).

---

## 📊 Dataset Overview
The dataset analyzed (`indian_tech_jobs_2026.csv`) contains **23,201 rows** (job postings) and **32 columns** (features) detailing:
*   **Job Metadata:** Job ID, job titles, URLs, and descriptions.
*   **Company Information:** Company names, ratings, and size buckets.
*   **Location:** Specific neighborhood locations, scraped cities, and standardized primary cities.
*   **Experience & Education:** Raw experience requirements, minimum/maximum years, and experience tiers.
*   **Salaries:** Raw salary ranges, minimum/maximum LPA (Lakhs Per Annum), midpoint LPA, and salary tiers.
*   **Skills:** Required skills and skill domains (e.g. Business Intelligence, AI/ML/DL, DevOps).
*   **Workplace Models:** Work modes (Remote, Hybrid, On-site) and fresher-friendliness markers.

---

## 🔍 Key Insights & Answer Dashboard

### 1. Which cities pay the most for Data Scientists?
Based on the mean and median salary midpoints (in LPA) for cities with at least 5 disclosed salaries:
*   **Hyderabad** leads the country with a mean of **22.18 LPA** (median **22.50 LPA**).
*   **Pune** follows closely with a mean of **20.50 LPA** (median **20.00 LPA**).
*   **Bangalore** (often considered the primary IT capital) ranks third with a mean of **20.36 LPA** (median **20.50 LPA**).
*   **Delhi** and **Gurgaon** round out the top five with means of **20.31 LPA** and **19.88 LPA**, respectively.

*Insight:* While Bangalore has a massive volume of tech jobs, Hyderabad and Pune pay a premium for Data Science talent due to a larger concentration of senior-level postings.

| Rank | Cleaned City | Mean Salary (LPA) | Median Salary (LPA) | Postings Count |
| :---: | :--- | :---: | :---: | :---: |
| 1 | **Hyderabad** | 22.18 | 22.50 | 31 |
| 2 | **Pune** | 20.50 | 20.00 | 120 |
| 3 | **Bangalore** | 20.36 | 20.50 | 40 |
| 4 | **Delhi** | 20.31 | 17.50 | 41 |
| 5 | **Gurgaon** | 19.88 | 18.50 | 68 |

---

### 2. Which skills command the highest salary premium?
Looking at specific skills extracted from job requirements (filtering for skills with at least 30 disclosed postings):
*   **Predictive Modeling** commands the highest average compensation of **26.98 LPA**.
*   **Retrieval Augmented Generation (RAG)** and **Agentic AI** command averages of **25.49 LPA** and **25.13 LPA**, respectively.
*   **Gen AI / Generative AI** and **Natural Language Processing (NLP)** follow with means of **24.47 LPA** and **24.09 LPA**.
*   Engineering practices like **CI/CD** (23.84 LPA) and **MLOps** (23.22 LPA) also command significant premiums.

*Insight:* Modern AI engineering, Generative AI (RAG, LLMs, LangChain), and MLOps are the most financially rewarded competencies in 2026.

| Rank | Skill | Mean Salary (LPA) | Median Salary (LPA) | Postings Count |
| :---: | :--- | :---: | :---: | :---: |
| 1 | **Predictive Modeling** | 26.98 | 26.00 | 38 |
| 2 | **RAG (Retrieval Augmented Gen)** | 25.49 | 22.38 | 40 |
| 3 | **Agentic AI** | 25.13 | 22.50 | 78 |
| 4 | **Gen AI** | 24.47 | 22.50 | 39 |
| 5 | **Natural Language Processing (NLP)** | 24.09 | 22.50 | 118 |

---

### 3. Remote vs. Hybrid vs. On-site trends across roles
*   **On-site is the dominant model** across all tech roles, representing **74% to 87%** of all postings.
*   **Machine Learning Engineers** have the highest flexibility, with **15.41%** of jobs offered as **Remote**.
*   **Data Scientists** (10.50%) and **Data Engineers** (10.20%) also have higher-than-average remote rates.
*   **Python Developers** are rarely remote (1.83%) but have the highest **Hybrid** adoption rate (**14.56%**).

| Role Category | Hybrid (%) | On-site (%) | Remote (%) |
| :--- | :---: | :---: | :---: |
| **Business Analyst** | 7.21% | 87.19% | 5.59% |
| **Data Analyst** | 5.98% | 85.96% | 8.06% |
| **Data Engineer** | 14.20% | 75.60% | 10.20% |
| **Data Scientist** | 12.94% | 76.56% | 10.50% |
| **Machine Learning Engineer** | 9.99% | 74.60% | **15.41%** |
| **Python Developer** | **14.56%** | 83.61% | 1.83% |

---

### 4. Fresher opportunity mapping across cities
*   **Absolute Volume:** **Mumbai** offers the highest number of entry-level opportunities with **633** fresher-friendly jobs, followed by **Noida** (545) and **Gurgaon** (441).
*   **Relative Percentage:** Among major cities, **Ahmedabad** has the highest proportion of fresher jobs (**25.83%**), followed by **Kolkata** (23.33%) and **Noida** (21.08%).
*   **Experience-Driven Hubs:** **Hyderabad** has the lowest fresher-friendly ratio (**7.05%**), indicating a strong preference for experienced talent.

| Cleaned City | Fresher-Friendly Jobs | Total Job Postings | Percentage (%) |
| :--- | :---: | :---: | :---: |
| **Mumbai** | 633 | 3,382 | 18.72% |
| **Noida** | 545 | 2,585 | 21.08% |
| **Gurgaon** | 441 | 2,210 | 19.95% |
| **Kolkata** | 418 | 1,792 | 23.33% |
| **Chennai** | 401 | 2,718 | 14.75% |
| **Remote** | 395 | 2,010 | 19.65% |
| **Pune** | 383 | 2,693 | 14.22% |
| **Bangalore** | 379 | 2,830 | 13.39% |
| **Ahmedabad** | 358 | 1,386 | **25.83%** |
| **Hyderabad** | 38 | 539 | **7.05%** |

---

### 5. Which companies hire the most for ML roles in India?
Filtering for jobs in the *Machine Learning Engineer* role category or *AI/ML/DL* skill domain, the top recruiters are:
1.  **Tata Consultancy Services (TCS):** 194 jobs
2.  **Accenture:** 132 jobs
3.  **Paytm:** 95 jobs
4.  **Infosys:** 73 jobs
5.  **Welo Data:** 60 jobs
6.  **Capgemini:** 57 jobs
7.  **Fractal Analytics:** 52 jobs
8.  **Nagarro:** 50 jobs
9.  **Thales:** 49 jobs
10. **Leading Client:** 44 jobs

---

## 🛠️ Setup & Requirements
To run this notebook locally, ensure you have a Python environment set up with the following libraries installed:

```bash
pip install numpy pandas matplotlib seaborn wordcloud
```

### Running the Notebook
1. Clone this repository to your local machine.
2. Open a terminal and run `jupyter notebook` or open the workspace in VS Code.
3. Open `edaITjobs.ipynb`.
4. Run all cells in sequence. The notebook contains detailed headings and explanations for each step.

---

## 📈 Exploratory Analysis Sections
The Jupyter Notebook is organized into logical sections:
1.  **Project Title & Introduction**: Project metadata and objectives.
2.  **Importing Libraries**: Importing standard data structures and visualization packages.
3.  **Data Loading**: Ingesting the CSV file.
4.  **Initial Data Exploration**: Visualizing dataframe dimensions, null values, datatypes, and summary statistics.
5.  **Univariate Analysis (Categorical)**: Charting distributions of job roles, cities, work modes, and experience levels.
6.  **Univariate Analysis (Numerical)**: Plotting distributions of ratings, minimum experience, and salaries.
7.  **Bivariate and Multivariate Analysis**: Scatter plots, box plots, top hiring company charts, a correlation heatmap, and word cloud.
8.  **EDA & Insights Dashboard**: Dynamic Python queries and summary tables answering the 5 research questions.
# IndianITjobs2026-Analysis
