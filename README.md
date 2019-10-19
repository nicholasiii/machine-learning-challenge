# machine-learning-challenge
0I attempted three different machine-learning models on this data: A neural net, a multilinear regression, and a random forest. This was challenging due to my limited computing power, but Google Colab came through so I could run the Neural Net. Of the three the regression was by far the worst. It could only successfully predict one third of the results.

The Random Forest Model took the most time to fine-tune, and was better than the regression. It also proved extremely useful in debugging: all models were suspiciously accurate, and when I outputted the forest to a graphics fie I discovered this was because I had left in two columns: koi_disposition_CANDIDATE and koi_disposition_FALSE POSITIVE. If there’s a zero in both those columns then there has to be a one in the koi_disposition_CONFIRMED column and that’s the answer.

After running it with all 42 variables I had an R-Score of 64.6%, and a mean error of 0.37. I tried multiple permutations of variables. I eyeballed the output graph, picked the seven most important and ran various combinations of then. The mean error was always exactly 0.37, and the accuracy never went above 55%. Then I added three more and got the same result. So the Random Forest does work, but you can’t prune the variables down from 42 and improve the result.

Neural Net was the most successful. It predicted 90.88% of the planets with a loss of only 23.19%. It was by far the most difficult to get working. Every-time I tried to run it on my laptop Jupyter would inform me that “the kernel died” when trying to run the first Epoch, and my desktop wouldn’t even load all the Tensorflow and SKLearn modules much less run the script.

