# Pet Adoption Prediction

This project focuses on predicting whether a pet will be adopted or not using a deep neural network implemented in Keras. The dataset used in this project contains information about pets, including their type, age, breed, gender, and other attributes.


## Dataset

The dataset contains information about pets and includes the following columns:

| Column          | Description |
|-----------------|-------------|
| Type            | Type of animal (e.g., Cat, Dog) |
| Age             | Age of the pet in months |
| Breed1          | Primary breed of the pet |
| Gender          | Gender of the pet |
| Color1          | Primary color of the pet |
| Color2          | Secondary color of the pet (if any) |
| MaturitySize    | Size of the pet when fully grown |
| FurLength       | Length of the pet's fur |
| Vaccinated      | Vaccination status of the pet |
| Sterilized      | Sterilization status of the pet |
| Health          | Health status of the pet |
| Fee             | Adoption fee |
| Description     | Description of the pet |
| PhotoAmt        | Number of photos uploaded |
| AdoptionSpeed   | Speed of adoption (target variable) |

The **AdoptionSpeed** column is the target variable and indicates how quickly a pet was adopted. The values are as follows:

- **0**: The pet was adopted on the same day it was listed.
- **1**: The pet was adopted within 1-7 days.
- **2**: The pet was adopted within 8-30 days.
- **3**: The pet was adopted within 31-90 days.
- **4**: The pet was not adopted after 100 days.

## Model Training

A deep neural network is implemented using Keras. The model consists of:

- **Input Layer**: 26 input features.
- **Hidden Layers**: Three hidden layers with 128, 64, and 32 neurons, respectively, using ReLU activation.
- **Output Layer**: A single neuron with a sigmoid activation function for binary classification.

The model is trained using the Adam optimizer and binary cross-entropy loss. The training process includes:

- **Data Preprocessing**: Categorical features are encoded using LabelEncoder and BinaryEncoder. Numerical features are standardized.
- **Training**: The model is trained for 10 epochs with a batch size of 128.
- **Validation**: The model's performance is evaluated on a validation set during training.

## Model Performance

The model achieved the following F1 scores:
- **Training Set**: 0.77
- **Test Set**: 0.72

## Requirements

To run this project, you need the following Python libraries:
- numpy
- pandas
- scikit-learn
- keras
- category_encoders
