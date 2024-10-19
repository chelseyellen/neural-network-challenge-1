# Neural Network Challenge Part 1

## Intro
This challenge asked us to design a neural network model to process data associated with student loans to determine the credit quality of a student based on the features in the dataset. This entailes considering the number of inputs, determine the number of layers of my models, and the number of neurons on each layer. Then I will compile and fit my model, and evaluate the model to calculate its loss and accuracy.

## Part 1: Prepare the data for use on a neural network model
I utilized the following steps to preprocess the data using Pandas & StandardScaler:
* Utilized the starter data
* Read the data from https://static.bc-edx.com/ai/ail-v-1-0/m18/lms/datasets/student-loans.csvLinks to an external site into a Pandas DataFrame. 
* Reviewed the DataFrame and looked for columns that could eventually define my features and target variables.
* Created the features (X) and target (y) datasets as defined by the “credit_ranking” column. The remaining columns defined the features dataset.
* Split the features and target sets into training and testing datasets.
* Used scikit-learn's StandardScaler to scale the features data.

## Part 2: Compile and Evaluate a Model Using a Neural Network
I utilized my knowledge of TensorFlow to design a deep neural network model using the dataset’s features to predict the credit quality of a student based on the features in the dataset.
* Created a deep neural network by assigning 1 as the number of input features, 2 input layers, and utilized 6 neurons/nodes for the first layer and 3 neurons/modes for the second layer using TensorFlow’s Keras.
* I compiled the Sequential model and fir it using the binary_crossentropy loss function, the adam optimizer, and the accuracy evaluation metric
* I evaluated the model using the test data to determine the model’s loss and accuracy
* Then I cased and exported my model to a keras file, and named the file student_loans.keras
* Note: I did this all in VSCode, and not Colab

## Part 3: Predict loan repayment success by using the neural network model
I used the model saved in the previous section to make predictions on the reserved testing data.
* I reloaded the saved model
* I made predictions on the testing data
* Then I saved them to a DataFrame and rounded the predictions to binary values
* I generated a classification report with the predictions and testing data

## Part 4: Discuss creating a recommendation system for student loans
**1. Describe the data that you would need to collect to build a recommendation system to recommend student loan options for students. Explain why this data would be relevant and appropriate.**
 * Student Demographics: Age, location, and family income would be important to understand the credit/financial background of the individual and loan eligibility
 * Loan history: Debt to income ratio, repayment history, and credit score would outline creditworthiness for eligibility of products
 * Loan details: Amount of loan, interest rate, repayment length/terms, etc. would be needed to recommend the right loan to the student
 * Academic information: Year of graduation can be used to outline load terms 

 This data is needed to understand creditworthiness, credit history, and personal financial needs to personalize the appropriate loan for the student based upon their circumstances.


**2. Based on the data you chose to use in this recommendation system, would your model be using collaborative filtering, content-based filtering, or context-based filtering? Justify why the data you selected would be suitable for your choice of filtering method.**

The model would use content-based filtering as the features of the loan would be used to address the needs of this specific student. This method is suitable because the recommendation system relies on specific attributes of the students (demographics, academic information, loan history) and loan products (interest rates, repayment terms) to make recommendations.

**3. Describe two real-world challenges that you would take into consideration while building a recommendation system for student loans. Explain why these challenges would be of concern for a student loan recommendation system.**

Bias in the algorithm could favor one group of students over another, which would lead to a disadvantageous recommendation for certin groups or advantageous loan recommendations for another group. This is a concern as students should have equal access to higher education, and loans are a key component to that access for socioeconomically diverse students.

Data privacy and secturity is also always a concern when dealing with highly sensitive data that identifies individuals and their financial situations. A good recommendation system must adhere to laws and regulations based upon the location in which they sit jurisdictionally. 