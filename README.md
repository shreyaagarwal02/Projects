# Car-Price-Prediction
The Car Price Prediction Model is a machine learning project designed to estimate the resale value of used cars by analyzing a dataset containing various attributes such as the car's name, company, year of manufacture, kilometers driven, and fuel type. This project begins with the importation of essential Python libraries, including Pandas and NumPy, for data manipulation and processing.

The dataset is loaded and examined to understand its structure. Initial steps involve cleaning and preprocessing the data to ensure its suitability for modeling. The dataset is filtered to remove entries with non-numeric year values and those with missing or inconsistent price and mileage information. The car prices are converted from strings to integers after removing commas, and entries with unreasonable prices are discarded to avoid skewing the results. Similarly, the kilometers driven are cleaned and converted to numeric values.

The car names are simplified by limiting them to the first three words, which helps in standardizing the entries and reducing complexity. The dataset is then reset to ensure that all indices are in order.

Once the data is cleaned, it is split into features (X) and the target variable (y), where X includes attributes like car name, company, year, kilometers driven, and fuel type, while y represents the car price. The dataset is then split into training and testing sets using the train_test_split function.

The model is built using Linear Regression, with categorical variables like car name, company, and fuel type being encoded using OneHotEncoder. This encoding is applied within a pipeline that combines the transformation and the regression model, streamlining the process.

The model is trained on the training set and evaluated using the R-squared score, which measures how well the model predicts the car prices. The project also includes a loop that iterates 1,000 times to find the optimal train-test split with the highest R-squared score.

Finally, the trained model is saved using Python's pickle module, allowing for future use without retraining. A sample prediction is made to test the model, demonstrating its ability to estimate car prices based on specific inputs.







