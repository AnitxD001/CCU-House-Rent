# Kolkata House Rent Prediction

This project predicts house rent in Kolkata based on multiple features like the number of bedrooms, area, bathrooms, locality, property type, and furnishing type. The Random Forest Regressor model is used for making the final predictions, as it turned out to provide the best results among the models tested.

## Features Used

The model considers the following input features:

1. **Number of Bedrooms**
2. **Area (in sq. ft.)**
3. **Number of Bathrooms**
4. **Property Type**:
   - Apartment
   - Independent House
   - Independent Floor
   - Studio Apartment
   - Villa
5. **Locality**: Various localities in and around Kolkata, such as:
   - Action Area I
   - Ballygunge
   - Salt Lake City
   - Behala
   - New Town
   - Garia, and more
6. **Furnishing Type**: 
   - Furnished
   - Semi-Furnished
   - Unfurnished

## Models Tested
Several models were evaluated to determine the best one for this prediction task, including:
- **Linear Regression**
- **Lasso**
- **Support Vector Classifier (SVC)**
- **Random Forest Regressor** *(Best Performing Model)*

## How It Works
The application takes user input for features like the number of bedrooms, area, bathrooms, property type, locality, and furnishing type. Based on these inputs, the Random Forest model is used to predict the house rent. The model was trained using data from various properties in Kolkata.

## Setup and Installation

1. Download the dataset CSV file and place it in the project directory. Ensure that the dataset is named `Kolkata_rent.csv`.

2. Run the prediction script:
   ```bash
   python kolkata house rent.ipynb
   ```

That's it! The script will use the provided dataset to train the model and make predictions based on user inputs.
You can refer to the list of locations text file to get a view of all the locations used in the prediction model

## Usage
Once the setup is complete, you can input the required details to get the predicted house rent for a property. The script will ask for:
- Number of bedrooms
- Area in square feet
- Number of bathrooms
- Property Type (Apartment, Independent House, etc.)
- Locality
- Furnishing Type (Furnished, Semi-Furnished, or Unfurnished)

The model will then output the predicted rent.

## Example

```bash
Enter number of bedrooms: 3
Enter area in square feet: 2500
Enter number of bathrooms: 2
Is it an Apartment? (1 for Yes, 0 for No): 0
Is it an Independent Floor? (1 for Yes, 0 for No): 1
Is it an Independent House? (1 for Yes, 0 for No): 1
Is it a Studio Apartment? (1 for Yes, 0 for No): 0
Is it a Villa? (1 for Yes, 0 for No): 1
Enter locality (choose from the listed localities): Elgin
Choose furnishing type:
1: Furnished
2: Semi-Furnished
3: Unfurnished
Enter your choice (1, 2, or 3): 2
The predicted rent: 42600.0
```

## Model
The model used for the final predictions is **Random Forest Regressor**, which provided the best results during testing and evaluation. It is configured with the following hyperparameters:
- `n_estimators`: 20
- `max_depth`: 10
- `min_samples_split`: 2
