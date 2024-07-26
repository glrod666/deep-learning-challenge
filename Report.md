# Report on Neural Network Model Performance

## Purpose of the Analysis
The purpose of this analysis is to build and evaluate a neural network model to predict binary outcomes. We will test different configurations of hidden layers and activation functions to find the best model.

## Model Building and Evaluation

### First Attempt
**Model Configuration:**
- 2 hidden layers with 8 and 5 nodes respectively.
- Activation function: ReLU (Rectified Linear Unit) for both hidden layers.
- Output layer with 1 node and sigmoid activation.

**Model Performance:**
- Accuracy: 72.91%
- Loss: 0.5512

*Summary: The model performed reasonably well with an accuracy of around 73%.*

### Second Attempt
**Model Configuration:**
- 2 hidden layers with 10 nodes each.
- Activation function: ReLU for both hidden layers.
- Output layer with 1 node and sigmoid activation.

**Model Performance:**
- Accuracy: 73.03%
- Loss: 0.5511

*Summary: Increasing the number of nodes in hidden layers slightly improved the accuracy, but the difference is minimal.*

### Third Attempt
**Model Configuration:**
- 2 hidden layers with 20 nodes each.
- Activation functions: Tanh for the first hidden layer, Sigmoid for the second.
- Output layer with 1 node and ReLU activation.

**Model Performance:**
- Accuracy: 46.24%
- Loss: 8.2926

*Summary: This configuration significantly decreased the model's performance. The choice of activation functions negatively impacted the results.*

## Results Analysis

 Questions 

1. **What was the initial accuracy of the model?**
   - The initial accuracy of the model was 72.91%.

2. **How did you decide on the number of input features and hidden nodes for each layer?**
   - The number of input features was determined by the dataset (length of `X_train[0]`). The hidden nodes were chosen based on common practices and trial and error.

3. **What activation functions were used in the hidden layers?**
   - In the first two attempts, ReLU was used for the hidden layers. In the third attempt, Tanh and Sigmoid were used.

4. **What was the impact of changing the number of hidden nodes on the model's accuracy?**
   - Increasing the number of hidden nodes from 8 and 5 to 10 and 10 slightly improved the accuracy from 72.91% to 73.03%. However, increasing to 20 and 20 with different activation functions drastically reduced the accuracy to 46.24%.

5. **How did the activation functions affect the model's performance?**
   - ReLU activation functions provided better performance. Using Tanh and Sigmoid in the hidden layers severely impacted the model's accuracy.

6. **What was the final model's accuracy, and how did it compare to the initial model?**
   - The final model's accuracy was 46.24%, which is significantly lower than the initial model's accuracy of 72.91%.

## Summary of Overall Results
The initial model with ReLU activation functions and a smaller number of hidden nodes performed the best, achieving an accuracy of approximately 73%. Increasing the nodes slightly improved the accuracy, but changing activation functions drastically reduced it.

## Alternative Model Approach
we could use a Random Forest classifier. Random Forests are robust and handle non-linear data well
 Benefits
- **Simplicity**: Easier to implement and interpret.
- **Performance**: Often performs well on a variety of problems without extensive tuning.
