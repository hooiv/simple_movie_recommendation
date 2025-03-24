# Movie Recommender System 🎬
This repository contains a Streamlit-based Movie Recommender System that uses TMDB data. The application demonstrates how to download a dataset from Kaggle, preprocess the data, create a simple recommendation engine, and then serve it via Streamlit.

## 🚀 Features

📌 Movie recommendations based on content similarity.

🎭 Uses movie genres, cast, director, and keywords for recommendations.

🎨 Displays movie posters using TMDB API.

🏎️ Runs in Google Colab using Streamlit and pyngrok for deployment.

- Downloads and preprocesses the TMDB 5000 Movie dataset from Kaggle.
- Merges movie and credits data for a complete dataset.
- Uses a basic Bag of Words approach with CountVectorizer to vectorize movie metadata.
- Computes similarity scores between movies using cosine similarity.
- Pickles the processed movies data and similarity matrix for quick loading.
- Builds a user interface with Streamlit for interactive recommendations.

## 📂 Dataset

The dataset used is TMDB 5000 Movie Dataset available on Kaggle.

## Workflow
1. Install dependencies and set up the Kaggle environment (including placing your `kaggle.json` credential file in the appropriate directory).
2. Download the TMDB data from Kaggle (`tmdb-movie-metadata.zip`).
3. Unzip and merge movie data (including credits).
4. Preprocess data by extracting genres, cast, crew, and keywords.
5. Vectorize the resultant tags (metadata) using CountVectorizer with English stop words removed.
6. Compute cosine similarity among movie vectors.
7. Build a Streamlit app (`app.py`) which:
   - Allows users to select a movie from a dropdown.
   - Recommends top 5 similar movies along with their posters.
8. Launch Streamlit using ngrok to create a public URL for the running application.

## Usage
1. Clone the repository and navigate to the project directory:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```
2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```
3. Place your `kaggle.json` file in the correct directory (as shown in the code) and run the preprocessing steps to download and unzip the TMDB dataset.
4. Run the `app.py` with Streamlit:
   ```bash
   streamlit run app.py
   ```
5. Access the provided local or ngrok URL in your browser.

## Project Structure
- `app.py`: Streamlit application for the recommender system.
- `movie_list.pkl` & `similarity.pkl`: Pickled files for the processed dataset and precomputed similarity matrix.
- `tmdb-movie-metadata.zip`: Downloaded dataset from Kaggle (not included in this repo).
- `README.md`: Documentation and usage instructions for this project.
## 📜 License
This project is licensed under the MIT License.
Please check the Kaggle TMDB data license terms before commercial or large-scale usage. This project is provided for educational and demonstration purposes.

## ✨ Contributions
Feel free to fork the repository and submit a pull request if you have any improvements!


## 🚀 Happy Coding! 🎥
