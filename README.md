# Book-Recommendation-System
A Book Recommendation System built using Python and collaborative filtering to recommend books based on user rating patterns.

The system analyzes book ratings, identifies popular and frequently rated books, creates a user-book rating matrix, and uses cosine similarity to find books that are similar to a selected book.

🚀 Project Overview

The goal of this project is to build a recommendation system that can suggest books to users based on similarities in rating behavior.

The project uses the Book-Crossing dataset, containing information about:

📖 Books
👤 Users
⭐ Book ratings

The dataset contains approximately 271K ratings, 114K users, and 278K users records/books-related data, which was explored and processed during the project.

🛠️ Technologies Used
Python
Pandas – Data manipulation and analysis
NumPy – Numerical operations
Scikit-learn – Cosine similarity
Jupyter Notebook – Development and experimentation
🔄 Project Workflow
Book-Crossing Dataset
        ↓
Data Loading
        ↓
Data Cleaning & Exploration
        ↓
Rating Analysis
        ↓
Filter Active Users
        ↓
Filter Frequently Rated Books
        ↓
Create User-Book Rating Matrix
        ↓
Fill Missing Ratings
        ↓
Calculate Cosine Similarity
        ↓
Generate Book Recommendations
📊 Data Processing

The project begins by loading three datasets:

Books.csv
Users.csv
Ratings.csv

The data was examined for:

Missing values
Duplicate records
Data types
Rating distributions
User age distribution
Number of ratings per book

The user dataset contains missing values in the Age column, which was also explored during analysis.

⭐ Popular Books Analysis

Book ratings were aggregated to calculate:

Number of ratings per book
Average rating per book

Books with at least 250 ratings were considered for the popular-book analysis.

Examples of highly rated/popular books identified during the analysis include:

Harry Potter series
The Hobbit
The Lord of the Rings
To Kill a Mockingbird
The Da Vinci Code
The Lovely Bones
1984
🤖 Recommendation System

The recommendation system uses collaborative filtering.

First, users with more than 200 ratings were selected to focus on active readers.

Then, books with at least 50 ratings among these users were selected.

This resulted in a user-book matrix containing:

706 books × 810 users

Missing ratings were filled with 0 before calculating similarity.

📐 Cosine Similarity

The system uses cosine similarity to measure how similar two books are based on their rating patterns.

from sklearn.metrics.pairwise import cosine_similarity

similarity_scores = cosine_similarity(pt)

The recommendation function takes a book name as input and returns the top 5 similar books.

Example:

recommend('The Da Vinci Code')

The system can then return books with similar user-rating patterns.

💡 Example Recommendation

For:

The Da Vinci Code

The system generates recommendations such as:

Angels & Demons
Touching Evil
Saving Faith
The Sweet Potato Queens' Book of Love
Middlesex: A Novel
📁 Project Structure
Book-Recommendation-System/
│
├── Book Recommendation.ipynb
├── README.md
├── Books.csv
├── Users.csv
├── Ratings.csv
└── requirements.txt

Dataset files can be excluded from the repository if they are too large or have separate distribution/licensing requirements.

⚙️ Installation

Clone the repository:

git clone https://github.com/your-username/book-recommendation-system.git

Navigate to the project directory:

cd book-recommendation-system

Install the required libraries:

pip install pandas numpy scikit-learn jupyter

Run Jupyter Notebook:

jupyter notebook

Open the project notebook and run the cells.

🎯 Key Skills Demonstrated
Data Cleaning
Exploratory Data Analysis
Data Preprocessing
Pandas & NumPy
Collaborative Filtering
Recommendation Systems
Cosine Similarity
Feature Matrix Creation
Data Analysis using Python
🔮 Future Improvements

The project can be further improved by adding:

A web interface using Streamlit or Flask
Book cover images
User-based recommendations
Hybrid recommendation techniques
Better handling of cold-start users
Recommendation ranking and evaluation metrics
Search/autocomplete functionality
Deployment as a web application
👨‍💻 Author

Sagar Verma

Business Analyst | Data Analyst | AI & Data Enthusiast
