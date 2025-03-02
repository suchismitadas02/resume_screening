# Resume Analysis and Ranking System

## Overview

This project is designed to analyze and rank resumes based on their relevance to a given job description. It uses Natural Language Processing (NLP) techniques to extract key skills, compute similarity scores, and rank resumes accordingly. The system is built using Python and leverages popular libraries such as Pandas, Scikit-learn, and spaCy.

## Features

- **Resume Cleaning**: Automatically cleans and preprocesses resume text by removing special characters, HTML tags, and stopwords.
- **Skill Extraction**: Extracts key skills from resumes using a predefined list of skills and spaCy's PhraseMatcher.
- **TF-IDF Vectorization**: Converts resume text into numerical features using Term Frequency-Inverse Document Frequency (TF-IDF).
- **Cosine Similarity**: Computes the similarity between resumes and a job description using cosine similarity.
- **Ranking**: Ranks resumes based on their similarity to the job description.
- **Visualization**: Provides visual insights into the distribution of job categories and the most common skills in the dataset.

## Installation

To run this project, you need to have Python installed on your system. Follow these steps to set up the environment:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/resume-analysis.git
   cd resume-analysis
   ```

2. **Install Required Libraries**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download spaCy Model**:
   ```bash
   python -m spacy download en_core_web_sm
   ```

## Usage

1. **Load the Dataset**:
   Ensure your dataset is in CSV format and contains at least two columns: `Category` and `Resume`. Update the file path in the script to point to your dataset.

2. **Run the Script**:
   Execute the Python script to analyze and rank resumes:
   ```bash
   python resume_analysis.py
   ```

3. **Review the Output**:
   - The script will generate a ranked list of resumes based on the provided job description.
   - The top 10 ranked resumes will be saved in an Excel file named `Ranked_Resumes.xlsx`.
   - Visualizations will be displayed in the console or saved as images.

## Code Structure

- **Data Loading and Preprocessing**:
  - Load the dataset and handle missing values.
  - Clean and preprocess the resume text.

- **Skill Extraction**:
  - Use spaCy's PhraseMatcher to extract skills from resumes.

- **TF-IDF Vectorization**:
  - Convert resume text into numerical features using TF-IDF.

- **Similarity Calculation**:
  - Compute cosine similarity between resumes and a job description.

- **Ranking and Visualization**:
  - Rank resumes based on similarity scores.
  - Generate visualizations for job category distribution and top skills.

## Example Output

### Top 10 Ranked Resumes

| Category      | Similarity_Score |
|---------------|------------------|
| Data Science  | 0.579239         |
| Data Science  | 0.579239         |
| Data Science  | 0.579239         |
| Data Science  | 0.579239         |
| Data Science  | 0.530256         |
| Data Science  | 0.530256         |
| Data Science  | 0.530256         |
| Data Science  | 0.530256         |
| Data Science  | 0.400261         |
| Data Science  | 0.400261         |

### Visualizations

- **Distribution of Job Categories**:
  ![Job Category Distribution](job_category_distribution.png)

- **Top 10 Most Common Skills**:
  ![Top Skills](top_skills.png)

## Dependencies

- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- spaCy
- Matplotlib
- Seaborn

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.
