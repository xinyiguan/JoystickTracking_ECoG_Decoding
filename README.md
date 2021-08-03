# Machine Learning Approach to Decode Motor-related Activity from ECog Data


#### Background
Given the known literature, localised populations of neurons represent specific directions of movement of external events and motor plans. Using a linear combination of spectral measures and time domain features, Schalk et al (2007, JNE) were able to predict kinematic parameters with an average Pearson’s r of 0.49, and demonstrate directional tuning of certain populations. We hypothesized that, using updated methodology, we could outperform both the prediction of kinematic parameters, as well as infer further information about the underlying neuronal structures.  

#### Method
The dataset consisted of 4 participants all fitted with intracranial ECog arrays, over the fronto-parietal cortex. The task involved participants continuously tracking a target with a joystick. Kinematics are measured as X-Y coordinates of the cursor position during the joystick tracking task. This serves as an inference to the related hand position and movement.
ECog data was filtered into frequency bands. The power spectrum and filtered data was used as inputs to the linear regression model.

#### Results
Feature importances were used to deduce a.) which electrodes best captured the motor representation of cursor position, and, b.) in which frequency bands this is best represented. Implications of these feature importances to both brain-computer interfaces (BCI’s) and human motor control are discussed.
The data was split into training and test folds with model optimization going through K-fold cross validation on the training set only. Hyper-parameters of penalty and learning rate were tuned. Additionally, ECog data was phase lagged between 0-100ms to optimise temporal tuning. Validated on data in which the spatial structure was randomly resampled. The model’s predictions are also visualised to provide an intuitive representation of the model’s accuracy of decoding X-Y coordinates.

#### Implications

This study demonstrates the ability to capture the human brain’s coding of spatial representation. Additionally, the ability to decode and predict the exogenous state (hand position) from the endogenous state (neural activity), with a high level of accuracy. Further research may utilise this procedure in an online BCI protocol to allow movement and manipulation of prostheses.
