# Machine Learning Trading

## Summary
In this Challenge, I'll assume the financial advisor role at one of the world's top five financial advisory firms. My firm competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, my firm has profited heavily by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave my firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. I plan to improve the existing algorithmic trading systems and maintain the firm's competitive advantage in the market. To do so, I'll enhance the current trading signals with machine learning algorithms that can adapt to new data.

## Conclusion
I began by working on the baseline model that my firm currently has. After running a classification report, the model performed poorly on accuracy and had low F1 scores for the signal to sell the short stock. I began tuning up the baseline model by increasing the short and long window, increasing the accuracy by two decimal places. So instead, I chose to keep the short and long window the same but increase the training end time by three more months. I found that this model increases the accuracy and the precision score for the signal to sell the short stock. However, I was still unsatisfied with just tuning the model, so I decided to take a new approach by creating a new model. 

For this new model, I imported a new classifier, DecisionTreeClassifier. As with other classifiers, DecisionTreeClassifier takes as input two arrays: an array X, sparse or dense, of shape (n_samples, n_features) holding the training samples, and an array Y of integer values, condition (n_samples,), holding the class labels for the training samples. I began by using the original training data as the baseline model, then fitting another model with the new classifier. I believe this model outperformed the previous models due to having a higher score on precision, F1 score, and recall for the signal to sell. The only downside is that the F1 score for the signal to buy decreased while the accuracy of the whole model stayed relatively consistent.


<img width="416" alt="Screen Shot 2022-09-18 at 10 43 18 PM" src="https://user-images.githubusercontent.com/107083440/190946335-5460fb05-8f8b-47ac-8314-aeabb7964ec4.png">

<img width="416" alt="Screen Shot 2022-09-18 at 10 41 39 PM" src="https://user-images.githubusercontent.com/107083440/190946204-fe2582b5-e5a0-468d-8c55-1f9a9d92d0f5.png">
