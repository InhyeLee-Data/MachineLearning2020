ML Project #2 : Airplane Image Classification

V1. (Apr 2)


Both models had a very low FP rate.
PRC chosen over NN for this version for a Higher True Positive Rate.

The prediction of each model seems to vary every time the model runs even when all the feature/parameters remain unchanged. 

1. Overall Image treatment: <br>
I used canny edge detection this time. Played with sigma, low_threshold, high_threshold
-> Improved the performance

2. For PRC - SGDClassifier: <br>
A combination of lower alpha and a different penalty was used
-> Improved the performance

3. For NN - MLPClassifier: <br>
A combination of lower alpha, hidden_layer_sizes lowered from 100 to 75, solver changed to 'lbfgs'
-> Improved the performance
