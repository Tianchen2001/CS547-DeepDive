
# Project Conclusion

## Overview
This project investigates gasoline price prediction using historical data and machine learning models. By analyzing various features and leveraging predictive models, the project provides actionable insights into the factors affecting price changes.

---

## Data Selection
The final dataset includes:
1. **Weekly U.S. Net Imports of Crude Oil and Petroleum Products**:
   - Unit: Thousand Barrels per Day.
   - Highlights supply-side factors influencing prices.

2. **Date/Time**:
   - Accounts for temporal patterns and specific events impacting price dynamics.

Historical gasoline prices were explored during the initial analysis but were not included as direct features in the final modeling due to a focus on external and temporal influences.

---

## Models Used and Optimal Parameters
The final deep learning model was optimized through extensive hyperparameter tuning. Key configurations:

### Model Architecture
- **Input Layer**: Matches feature dimensions.
- **Hidden Layers**:
  - First Hidden Layer: 128 neurons, ReLU activation, Dropout of 0.2.
  - Second Hidden Layer: 64 neurons, ReLU activation, Dropout of 0.1.
- **Output Layer**: 1 neuron with linear activation for regression.

### Hyperparameters
- Optimizer: Adam.
- Loss Function: Mean Squared Error (MSE).
- Batch Size: 16.
- Epochs: 500.

### Performance Evaluation
- The final model achieved a **Mean Absolute Error (MAE)** of approximately $1.02 during the test phase.
- Training, validation, and test losses were monitored across epochs, confirming stability and generalization.

---

## Feature Importance
The permutation importance analysis revealed the following:

1. **Date**:
   - **Importance Score**: 1.0414.
   - The most influential feature, showcasing strong temporal dependency in gasoline prices. Disrupting this feature increased prediction error by approximately $1.02/gallon.
   - Suggests consistent patterns linked to economic cycles, seasonal demand, and significant events.

2. **Net Imports**:
   - Significant impact on predictions, emphasizing how variations in supply metrics directly affect pricing.

---

## Results and Insights

### Results
1. **Model Accuracy**:
   - The deep learning model demonstrated strong performance with a Mean Absolute Error (MAE) of $1.02 on test data, validating its ability to predict gasoline prices within a close range.
   - The model effectively captured the temporal dependencies and supply-side influences, showcasing stable performance across validation and test phases.

2. **Feature Importance Validation**:
   - The permutation importance analysis confirmed that date and net imports are the primary drivers of price changes.
   - This reinforces the notion that gasoline prices are influenced more by external and temporal factors than by intrinsic historical values.

### Insights
1. **Temporal Significance**:
   - The importance of the date feature highlights how strongly gasoline prices are tied to time-dependent patterns. These patterns may reflect broader economic cycles, geopolitical events, or predictable seasonal demand changes.
   - This insight can help consumers and businesses anticipate price shifts during key periods, such as holidays or geopolitical disruptions.

2. **Practical Budgeting**:
   - Accurate predictions allow individuals to better plan their fuel-related expenses, particularly during volatile economic periods or seasonal demand surges.

3. **Policy and Business Planning**:
   - Policymakers can rely on this model to anticipate price fluctuations and implement strategies to mitigate impacts on consumers.
   - Businesses, especially those in transportation, can leverage predictions to optimize logistics and reduce unexpected costs.

4. **Energy Sustainability**:
   - Insights into the significant role of imports underline the importance of investing in domestic energy production and renewable energy sources for greater economic stability and sustainability.

---

## Licensing
This project is shared under the MIT License, allowing free usage with appropriate attribution to the authors.

