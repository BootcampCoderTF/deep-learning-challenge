The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures.

# Report
 ----------

## Overview:

Alphabet Soup, a nonprofit foundation, seeks a tool to streamline the selection process for funding applicants with the highest probability of success in their endeavors. This will be done by using the provided CSV file by Alphabet Soup's business team, containing data on over 34,000 organizations previously funded by the foundation.

The objective is to leverage your expertise in machine learning and neural networks to develop a predictive model. This model will determine the likelihood of success for applicants if they receive funding from Alphabet Soup.

## Results:

Data Preprocessing

What variable(s) are the target(s) for your model?
The target variable for the model is IS_SUCCESSFUL, which indicates whether the charity donation was successful or not.

What variable(s) are the features for your model?
For all three models I decided to use all 43 features for the model since I was using a powerful tool like Google Colab, in other words, the feature variables for the model include all columns except IS_SUCCESSFUL.

What variable(s) should be removed from the input data because they are neither targets nor features?
The variables EIN and NAME were removed as they are neither targets nor features.

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
Model One:

Two hidden layers with 80 and 30 neurons respectively, followed by an output layer. This was just a base to begin from.

<img width="429" alt="nn_one_structure" src="https://github.com/BootcampCoderTF/deep-learning-challenge/assets/145591533/70765a8e-4e8b-4722-b1f4-cee953ffc160">

Model Two (Enhanced):

Three hidden layers with 80, 30, and 10 neurons respectively, followed by an output layer. The logic was that an increase in hidden layers would significantly increase the accuracy.

<img width="422" alt="nn_two_structure" src="https://github.com/BootcampCoderTF/deep-learning-challenge/assets/145591533/6517ecff-95c8-4b2f-be6d-5990ef24a1b0">

Model Three (Automated Tuning):

since manual adjustments felt like they weren't making significant progress, the architecture was tuned using Keras Tuner, resulting in a different architecture with multiple hidden layers and varying neuron counts.
It took 54 Trials and over 45mins to evaluate different models within the defined parameters

<img width="485" alt="nn_three_trails_results" src="https://github.com/BootcampCoderTF/deep-learning-challenge/assets/145591533/1ebf83a5-781f-47eb-891e-4239b5df676c">

This was the resulting Best Model

<img width="422" alt="nn_three_best_structure" src="https://github.com/BootcampCoderTF/deep-learning-challenge/assets/145591533/486d1877-5d99-4495-84ec-81120e97d10c">


Were you able to achieve the target model performance?

<img width="475" alt="nn_one_results" src="https://github.com/BootcampCoderTF/deep-learning-challenge/assets/145591533/bd22b191-ae7f-4564-926f-a182af3e49c8">. 

<img width="480" alt="nn_two_rsults" src="https://github.com/BootcampCoderTF/deep-learning-challenge/assets/145591533/c3fa0be1-282f-40bc-8f41-6f16fd3bb812">. 

<img width="497" alt="nn_three_final_results" src="https://github.com/BootcampCoderTF/deep-learning-challenge/assets/145591533/25ebde62-8341-40b3-b24e-22d0341ca35b">. 


Model One (52.96% accuracy), Model Two (57.76% accuracy), and Model Three (73.32% accuracy) did not achieve the target model performance. However, model Three came significantly close!

What steps did you take in your attempts to increase model performance?

Initially, manual adjustments were made to the architecture in Models One and Two, but they did not meet the target performance.
Automated hyperparameter tuning using Keras Tuner significantly improved model performance in Model Three.


## Summary:

The overall results indicate that manual adjustments to the neural network architecture were not sufficient to achieve the target performance. However, automated hyperparameter tuning proved to be effective in improving model performance. My recommendation would be to further refine the hyperparameters, particularly by increasing variables such as the maximum number of nodes and hidden layers. This would unfortunately increase testing time significantly which would have to be taken into consideration.

##### By Tafadzwa Fararira
