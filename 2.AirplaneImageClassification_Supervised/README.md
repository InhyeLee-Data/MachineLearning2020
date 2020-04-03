ML Project #2 : Airplane Image Classification

V1. (Apr 2)


Both models had a very low FP rate.
PRC chosen over NN for this version for a Higher True Positive Rate.

Question 1: The prediction of each model seems to vary every time it runs even when all the feature/parameters remain unchanged.
Question 2: Canny Edge Detection was used for this round. 
A plane's wings: Diagonal lines with curves. Straight lines of a aircraft body. Are they well recognized now? 
I am interested in trying out other methods. 

1. Overall Image treatment: <br>
Canny edge detection was used this time. Played with sigma, low_threshold, high_threshold

2. For PRC - SGDClassifier: <br>
A combination of lower alpha and a different penalty was used

3. For NN - MLPClassifier: <br>
A combination of lower alpha, hidden_layer_sizes lowered from 100 to 75, solver changed to 'lbfgs'
