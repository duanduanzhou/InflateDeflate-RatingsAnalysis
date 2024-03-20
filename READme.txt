Common Setup for Session 1,2, 3, and 4
Google Drive Preparation
* Create a folder named "CSE6242" in your Google Drive.
* Upload the following datasets and files:
       o For Data Preprocessing: 
              'meta-Georgia.json', 
              'review-Georgia.json'
       o For Recency Adustment:
       'complete_file_merged_filtered.csv'
       o For Fake Reviews Removal: 
              'combined_reviews.csv',
               'updated_filtered_atlanta_restaurant_reviews.csv'
       o For Data Analysis:
        'updated_filtered_atlanta_restaurant_reviews.csv', 'complete_file_merged_filtered_adjusted_1125.csv', 'complete_file_merged_filtered.csv'
Google Colab Configuration
* Open Google Colab and sign in with your Google account.
* Ensure that the GPU runtime is enabled for efficient processing:
       o Navigate to Runtime > Change runtime type.
       o Select GPU as the hardware accelerator.
Troubleshooting
* Ensure GPU support is enabled for efficient model training.
* Check the dataset file names and paths for accuracy.
* For memory issues, consider adjusting batch sizes or dataset sizes.


1. Data Pre-processing
* Open and Mount Drive: Open "DataPreprocessing.ipynb" and mount Google Drive.
* Data Loading: Load 'meta-Georgia.json' and 'review-Georgia.json'.
* Preprocessing: Perform data preprocessing to generate "filtered_atlanta_restaurant_reviews.csv".

2. Recency Adjustment:
RecencyAdjustment.ipynb
* Open and Mount Drive: Open "RecencyAdjustment.ipynb" and mount Google Drive.
* Data Loading: Load 'complete_file_merged_filtered.csv'.
* Recency Adjustment: Execute the steps in the notebook to adjust the data based on recency.
* Output: Generate the adjusted file "complete_file_merged_filtered_adjusted_1125.csv".

3. Fake Reviews Removal:
FakeDetectionBert.ipynb
* Open and Setup:
       o Upload or access "FakeDetectionBert.ipynb" in Google Colab.
       o Mount your Google Drive to access the datasets.
       o Install any required libraries and dependencies.
* Data Processing:
       o Load and preprocess the data from combined_reviews.csv.
* Model Training:
       o Train the BERT-based model on the dataset.
       o This may take some time due to the dataset size.
* Detection and Analysis:
       o Use the trained model to detect fake reviews in updated_filtered_atlanta_restaurant_reviews.csv.
       FakeDetectionCNN-LSTM.ipynb and FakeDetectionCNN-LSTM_Prediction.ipynb
* Open and Setup:
       o Upload or access "FakeDetectionCNN-LSTM.ipynb" and "FakeDetectionCNN-LSTM_Prediction.ipynb" in Google Colab.
       o Ensure your Google Drive is mounted and libraries are installed.
* Data Processing:
       o Follow the notebook to load and preprocess data.
* Model Training (FakeDetectionCNN-LSTM):
       o Train the CNN-LSTM-based model using combined_reviews.csv.
* Detection and Analysis (FakeDetectionCNN-LSTM_Prediction):
       o Run the "FakeDetectionCNN-LSTM_Prediction.ipynb" notebook.
       o Apply the trained model for detection on updated_filtered_atlanta_restaurant_reviews.csv.

4. Data Analysis and Visualization:
* Open and Mount Drive: Open "DataAnalysis_1.ipynb" and "DataAnalysis_2.ipynb" and mount Google Drive.
* Data Loading and Analysis: Load and analyze data from 'updated_filtered_atlanta_restaurant_reviews.csv', 'complete_file_merged_filtered_adjusted_1125.csv', and 'complete_file_merged_filtered.csv'.
* Visualization: Generate visualizations as shown in the report.

5. Interactive Map: 
Prerequisites
* Install latest version of Node.js (https://nodejs.org/en/ )
Setup and Running the Project
* (In case of error, delete package-lock.json file before you start.)
* Run npm install to install all packages in package.json needed for the project.
* Run npm start to run the application.
* It should automatically open the web link http://localhost:3000 in your default browser.
Purpose of Different Directories
* Images:
       o Under this directory, three screen shots of images for a demonstration of the web page are included. They are all embedded in the project readme file.
* Data-preprocess:
       o This directory includes an ipynb file which receives input from data processed after fake reviews removal and recency adjustment and outputs the csv files needed for this project. (you may run the file in google colab)
* Public:
       o Besides some setup files, data csv files after preprocessing are stored here. (specifically, atlanta_biz_data.csv and atlanta_biz_rating_percent_data.csv are two main data sources we used)
* Src:
       o Under this directory, all code for visualization is included.
       o Index.js, App.js, About.js, and Home.js are the JavaScript files for arranging the pages of the visualization web app.
       o Src/charts:
              * Under this directory, the configurations of all charts are included.
       o Src/components:
              * This directory includes the configuration for the filter bar feature.
              Video Demo for Interactive Map
              * YouTube Link: https://youtu.be/iyEandlyeTE?si=WgcSlC5iPHhnJ20V 


