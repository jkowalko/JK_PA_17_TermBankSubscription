# JK_PA_17_TermBankSubscription
This repo contains Practical Assignment 17, predicting customer purchase on a bank term subscription.



JK_Final_Bank_Prac3.ipynb

**Business Objective:**

The main goal of this project is to predict whether a potential bank client is likely to subscribe to a long-term deposit based on their characteristics and past interactions, and to use this prediction to improve the effectiveness of marketing campaigns. Essentially, we want to find the clients who are most likely to say "yes" to the offer before we even contact them, so we can focus our efforts on those most promising leads.

**Findings from analysis**

We looked at your historical data from previous marketing campaigns. We saw that most people contacted did **not** subscribe to the deposit. This is important because it means a simple prediction that no one will subscribe would be right most of the time (around 88% accurate). This "baseline" accuracy is a starting point, but it doesn't help us find the valuable clients who *will* subscribe.

We then tested a few different prediction models (like KNN, Logistic Regression, Decision Tree, and SVM) to see which one was best at identifying those who are likely to subscribe. We realized that just looking at overall accuracy wasn't enough because of the large number of people who didn't subscribe. We needed to look at how well the models found the people who *did* subscribe.

**Why the Decision Tree Model is Recommended:**

Based on our analysis, the **Decision Tree model** stands out as the most promising for your business objective. Here's why, in simple terms:

*   **Better at Finding Potential Subscribers:** While all models were good at identifying people who *wouldn't* subscribe, the Decision Tree was significantly better than the others at finding the people who *would* subscribe. Think of it like a better filter for finding the interested customers.
*   **Good Balance:** It does a good job of balancing between finding actual subscribers and not incorrectly flagging too many non-subscribers as interested. This means you're more likely to reach out to genuinely interested people and less likely to waste time on those who aren't.
*   **Easy to Understand:** Decision Tree models are relatively easy to understand. You can visually see the rules it uses to make predictions (like a flowchart), which can provide valuable insights into the characteristics of clients who are likely to subscribe.
*   **Faster to Use:** Compared to some other complex models we tested (like the SVM), the Decision Tree was much faster to train and use, making it more practical for real-world marketing campaigns and less computationally expensive. 

**Important Considerations:**

*   We excluded the 'duration' of the last call from the model used for prediction. While call duration is a strong indicator (longer calls often mean more interest), you don't know how long a call will last *before* you make it. Including it would make the predictions unrealistic for targeting.
*   The 'campaign' feature (number of times contacted) showed that more contacts in a campaign made a subscription less likely, which makes sense – people might get annoyed by too many calls.

**Next Steps and Recommendations:**

1.  **Implement the Decision Tree Model:** Integrate the tuned Decision Tree model into your marketing process.
2.  **Target Promising Leads:** Use the model to identify clients who are predicted to subscribe and prioritize contacting them.
3.  **Monitor Performance:** Continuously track how well the model's predictions translate into actual subscriptions in your campaigns. Monitor metrics like the conversion rate of clients identified as likely subscribers by the model.
4.  **Gather More Data:** Collect data on the outcomes of campaigns where you use this targeted approach. This new data can be used to further refine and improve the model in the future.
5.  **Explore Additional Features:** Consider if there are other relevant pieces of information you collect about clients that could be included in the model to potentially improve its predictions.
6.  **Consider Different Campaign Strategies:** Based on the insights from the Decision Tree (e.g., which clients are associated with subscription), you might tailor your marketing messages or approach for different client segments.

By using this Decision Tree model, you can move beyond a one-size-fits-all approach and make your marketing campaigns more efficient and effective by focusing on the clients who are genuinely most likely to be interested in your long-term deposit offer.
