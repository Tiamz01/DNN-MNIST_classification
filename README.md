# DNN-MNIST_classification
## Overview

This project is a image classification that deep neural network  to classify handwritten images(numbers). The project isused to master the ensorflow library for machine learning. The project also incorporates several data preprocessing steps that enhance the model or algorthm quality.

## Project Structure

The project can be divided into several key components:

1. **Data Collection**:
   - Data is collected from tensorflow dataset, the popular Mnist (handwritten) dataset: it includes image and labels.
   - The data is stored in npz format for tensorflow compactibility.

2. **Data Preprocessing**:
   - Data preprocessing is crucial to ensure that the data is clean and ready for analysis. In this project:
     - The data is splitted into 3, the train, validation and test dataset.
     - Data is the shuffled to enable randomness to avoid homogeneous data set since it will be utilizing the mini batch gradient descent algorithm.
     - Users who have rated more than 200 books are filtered to focus on active users.
     - Duplicates are removed based on user and book combinations.


3. **Machine Learning Model (DNN)**:
   - The model is built on Deep neural network frame with 784 iputs layer, 2 hidden layers of 50 depths and 10 outputs
   - The model structure is simple of linear combination and added activation function(non linearity) on the inputs that yield the hidden layers. The also processed the results using the rectifying linear unit(reLu) activation function. Since the task is a classfication task, softmax funnction.The softmax takes as argument the whole vector as every element in the outputs dpends on the entire set of the element in the inputs. The softmax transformation transform a the input to yield a probability distribution of the the outputs.
   -  

8. **Recommendation Function**:
   - A function, `recommend_book(book_name)`, is provided to suggest books to users.
   - The function finds the book's index in the pivot table, uses the k-NN model to identify similar books, and returns recommendations.

## Usage

To use the book recommendation system, follow these steps:

1. Ensure you have the required libraries installed (e.g., Pandas, NumPy, SciPy, Scikit-learn).

2. Load the dataset CSV files containing book, user, and rating data.

3. Run the data preprocessing steps to clean and merge the data.

4. Create the pivot table and sparse matrix for collaborative filtering.

5. Train the k-NN model on the sparse matrix.

6. Use the `recommend_book(book_name)` function to get book recommendations based on a specific book title.

## Future Enhancements

While this project provides a solid foundation for book recommendations, there are several areas for future enhancements:

- **Content-Based Filtering**: Incorporate book content features (e.g., genre, author) for more personalized recommendations.
- **Hybrid Filtering**: Combine collaborative and content-based filtering for improved recommendations.
- **Demographic Filtering**: Utilize user demographic data for more targeted suggestions.
- **Temporal Filtering**: Implement time-based recommendations, considering the publication year.
- **User Interface**: Develop a user-friendly interface for users to interact with the recommendation system.

Feel free to explore these enhancements to further enhance the quality and personalization of book recommendations.

---

This README provides an overview of the book recommendation project, explaining its approach, key steps, and filtering techniques. Follow the instructions to set up and use the recommendation system, and consider future enhancements for a more robust system.
