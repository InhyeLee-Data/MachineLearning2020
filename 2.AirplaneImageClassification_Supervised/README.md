## Airplane Image Classification Supervised Learning Progress Log

### V2 ([Final Notebook](), [csv](), May 1, 2020) 

#### Attempts to address issues which occurred in the previous model
In the previous submission, slightly different results were drawn upon running the same model with exact same settings. One suggestion from Aaron to tackle this issue was 
- Using a higher number for max_iter: Previously set to 1000
- Trying a larger learning rate: (Reference: Learning rate is between 0 and 1, larger values make the weight changes more volatile. By default, it is set to 0.001 in both models. For Perceptron, it seems that you can’t change this). 
- Or, the combination of the two.
in order to get to a gradient descent, which my model may not have been doing.

Changes were made, but I still had the same issue.

### V1 ([Notebook](Inhye_planeimages_V1_Submission.ipynb), [csv](airplane_submission_V1_re.csv), Apr 2 2020)

Both models had a very low FP rate.
Perceptron (PRC) chosen over Multi layer Neural Network (NN) for this version for a Higher True Positive Rate.

1. Overall Image treatment: <br>
Canny edge detection was used this time. Played with sigma, low_threshold, high_threshold

2. For PRC - SGDClassifier: <br>
A combination of lower alpha and a different penalty was used

3. For NN - MLPClassifier: <br>
A combination of lower alpha, hidden_layer_sizes lowered from 100 to 75, solver changed to 'lbfgs'

Question 1: The prediction of each model seems to vary every time it runs even when features/parameters remain unchanged. Why? <br>
Question 2: Canny Edge Detection was used for this round. A plane's wings have diagonal lines with connecting curves and an aircraft body has long & straight-ish lines. Are they well recognized in the feature now? I am interested in trying out other image processing methods. <br>
Question 3: There are only 21 airplanes (Positives) in the testing set (1690 pictures). So, missing one picture of an airplane greatly affects the TPR which is TP / (TP + FN). Would including more pictures of airplanes in this set change the prediction? 

