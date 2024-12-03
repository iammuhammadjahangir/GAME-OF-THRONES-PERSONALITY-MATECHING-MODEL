# Game of Thrones Personality Matcher

This application is designed to match a Game of Thrones character with the one whose personality traits are most similar. It utilizes **character embeddings** based on their dialogue and features a **visualization** of personality similarities between characters.

## Features

- **Character Selection**: Choose a character to find the closest match based on dialogue embeddings.
- **Character Visualization**: See the closest character match with images fetched from an external API.
- **Embedding-based Personality Matching**: Uses `TSNE` to map character dialogues into a 2D space, showing personality similarities.

## Setup

### Prerequisites

Make sure you have Python 3.6+ installed and the following dependencies:

- Streamlit
- NumPy
- Pandas
- Plotly
- TSNE (from Scikit-learn)
- Requests
- Pickle

You can install the required dependencies using `pip` by running:

````bash
pip install -r requirements.txt
Or manually install the required libraries:

bash
Copy code
pip install streamlit numpy pandas plotly scikit-learn requests pickle
File Structure
The project structure should look like this:

graphql
Copy code
GameOfThronesMatcher/
│
├── app.py                 # Main Streamlit app for character matching and visualization
├── data.pkl               # Pickled data containing character dialogue embeddings
├── script-bag-of-words.json # JSON file containing the dialogue data for characters
└── requirements.txt       # File listing project dependencies

## Running the Application

To run the Streamlit app, execute the following command in your terminal:

```bash
streamlit run app.py
## How to Use

- **Select a Character**: From the dropdown, select a character to see personality matches.
- **View Match**: The closest match will be displayed, along with the character images.
- **Visualize Data**: The app will also display a plot showing the position of characters in the personality space.

## Key Features in the App

- **Character Matching**: Find the closest personality match based on dialogue data.
- **Character Visualization**: Image representation of characters from the match.
- **Personality Visualization**: Use TSNE to project characters into a 2D space and visualize personality similarities.

## Sample Outputs

### Character Match

Displays the character with the closest match.

### Personality Visualization

A scatter plot showing characters in a 2D space based on their dialogue.

### Character Image

Displays the images of the selected character and their closest match fetched from an API.

## Files

### `app.py`
This file contains the core Streamlit application. It is responsible for uploading the character data, processing it, and displaying various statistics and visualizations.

### `data.pkl`
This is a pickle file that contains preprocessed data used for personality matching. It includes the x and y embedding values for each character.

### `script-bag-of-words.json`
This JSON file contains the dialogue data for each character used to generate the character embeddings.

## Customizing the App

### Modify Character Data
You can modify the `script-bag-of-words.json` file to include more characters and their dialogues. Re-run the code to generate new embeddings.

### Modify API Image Source
The images of characters are fetched from an external API (ThronesAPI). If you want to use a different API, update the `fetch_image()` function in `app.py`.
## Troubleshooting

- **App Not Loading**: Ensure all dependencies are correctly installed by running the `pip install` command.
- **Data Issues**: Ensure that the `data.pkl` and `script-bag-of-words.json` files are correctly formatted and available in the project directory.
- **Missing Character Images**: Ensure the API is accessible, or update the image fetching logic if needed.
````
