# Concatenate LSTM and Informer together

This time, I spent almost two weeks to rebuild the code as well as enlarge the sentimental analysis dataset. By rebuilding the code, I can easily switch my configuration in order to get the model with better performance. Then the method to concatenate two models seems very simple. I tried neural network, LightGBM and LinearRegression as the model to concatenate two models, then I found the most simple way, LinearRegression, is the best solution.

Then, the whole model structure is like below.

![Model Structure](./assets/ModelStructure.png)

<center>Fig 1 Model Structure</center>

To make the concatenation's usage more visible, I did the experiment on one stock, I will do the test on other stock in this week, and the results are here. We can see that the concatenation can actually lower the MSE. The plot for prediction part only and all data are shown below too. I will do these experiments on all stocks as soon as possible.

Also, I will try to use the pred of LSTM as the feature to train Informer or in reverse.

```
ConcatModel's MSE: 0.00011249626829225636
LSTM's MSE: 0.00017066089237121804
Informer's MSE: 0.005229426547884941
```

![image-20240819231716542](./assets/image-20240819231716542.png)

<center>Fig 2 Model's Performance on prediction data only</center>

![image-20240819231818320](./assets/image-20240819231818320.png)

<center>Fig 3 Model's Performance on all data</center>#   t i m e _ s e r i e s _ f o r c a s t i n g  
 