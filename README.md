# Motion_Prediction_of_Autonomous_Vehicles
Developement and implementation of deep learning algorithms to predict the behaviour of time series data - future states of vehicles - using the pre-processed inD dataset.
# Abstract:
Motion Prediction plays an important role in safety of drivers and passengers in autonomous vehicles. The
motion of a vehicle can be predicted using both Physics Based approach and Data Driven approach. This paper utilizes data
driven approach which involves the usage of deep learning neural networks namely Fully Connected Network (FCN), Long
Short-Term Memory (LSTM) and Recurrent Neural Network (RNN) for predicting position of vehicles in future time steps at
road intersections. Analyzing the results, it can be noticed that the FCN does not have required predictive characteristics for
this application. In order overcome this problem, LSTM and RNN were created. Even though LSTM provided good results
compared to FCN, RNN outperformed LSTM by a slight margin.

# Process Overview:

1. The dataset acquired from IND was too huge to be
processed completely by a normal computer. Since actual
data is not required to provide a good prediction, every 5th
frame was skipped to reduce the dataset size without losing
much information.
2. After skipping, the resulting data in the dataset was
normalized between 0 and 1, in order to simplify and
improve our processing speed.
3. After normalization, the data was split into 2. One set for
training the prediction modal, another for testing and
validation.
4. The training data was fed as input into the neural network
and the modal was trained for predicting the future values
in testing data.
5. After training, data from a specific recording ID was
provided as input for prediction testing.
6. The ground truth (actual data values of how the vehicle
moved in the time steps used for prediction) was collected
from the specific recording ID used for prediction testing.
7. Now, the output from the prediction testing obtained from
step 5 and the ground truth data read from the step 6 were
compared.
8. Using this comparison, 3 error values namely Average
Displacement Error (ADE), Final displacement error
(FDE) and Average Absolute Heading Error (AHE) were
calculated.
9. Based on these error values, the efficiency of the created
neural network modal was evaluated.
