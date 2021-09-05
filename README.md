# Hypothesis-testing-case-study

 The breakdown contains a sample of 1000 rows from our client’s online website sales. The extract has various information, but we will focus mainly on svar, showing us if the client was Male, Female, or not specified (empty cells) and the purchase value, pamount.
 ![image](https://user-images.githubusercontent.com/81958811/132121610-fb4d67fc-f76a-42ea-8bf6-14d2d1c4448c.png)



The new sales director that our client hired is sure that statistically speaking, there’s no difference between male and female spending and believes the marketing targets should not reflect gender. However, our client has a long experience in the business and believes that men generally spend more on tech. This should be reflected by allocating a higher portion of the marketing budget towards advertising to men.

They have asked you to resolve their argument and suggest how to proceed.

Let’s start by writing our hypothesis statement:

If an online tech shopper is a man, then their purchase value will be different (higher).

We can then denote our null hypothesis as the difference in means for both observation sets (Male and Female) is equal to zero. And the alternative hypothesis will be the exact opposite — the difference in the means is not zero, meaning the average purchase values for both sets are statistically different.

First, we can separate our observations into two groups, as we will be comparing the mean (average) purchase value by Males versus Females.

![image](https://user-images.githubusercontent.com/81958811/132121628-2737803e-dfd8-462b-94b5-c417e195f7ed.png)

Now, let’s run the Data Analysis menu from the Data tab on the Ribbon:

![image](https://user-images.githubusercontent.com/81958811/132121645-2f701037-5b7e-49e6-934e-2c8ae75a4525.png)

From the menu, select t-Test: Two-Sample Assuming Unequal Variances (as we don’t know the variances of the total populations):
![image](https://user-images.githubusercontent.com/81958811/132121652-084e7ae9-7407-455c-b9c9-0ae9777cba7f.png)


A dialog box opens up, where you will have to select the ranges for both variables (we now treat Males and Females as separate variables). Do not forget the check the Labels box if you select the headers of your data. The hypothesized mean difference will be zero, as per our null hypothesis.

In 99% of the cases, you can leave alpha at 0.05, as is, and you’ll be fine.

![image](https://user-images.githubusercontent.com/81958811/132121666-25eaa9fc-370e-4ff9-ac12-00cb7d549158.png)

Now run the analysis, and let’s look at the results.

The t-Test gives us some statistical information, but we are most interested in the two-tail p-value.

![image](https://user-images.githubusercontent.com/81958811/132121670-0885b80e-92ff-4480-aaa9-9269d829f879.png)

But why do we pick two-tail and not one-tail? Well, our null hypothesis is that the difference in means is = to zero. Then if we reject the null, this means the difference can be either above zero or below zero. Because of this, we pick the two-tail p-value. The best way to fully understand this concept is to draw a simple chart with two ‘tails’ for the alternative hypothesis. The red areas form the rejection region, and the green arrow points to the single value that is our acceptance region.
![image](https://user-images.githubusercontent.com/81958811/132121684-6209cef5-e7cd-4ed4-83bc-e275dbd5a307.png)


Therefore, we use the two-tail p-value of 0.038 and compare it to the alpha level of 0.05. The p-value is less than the level of significance (alpha), which means it is of statistical importance. We can reject the null hypothesis at the 95% confidence level. In conclusion, the data suggest that the difference between the average purchase value by males and females is significant. Therefore, it might be a good idea to do marketing separately.

Keep in mind the test result does not tell us if men spend more or less, just that there’s a statistically meaningful difference. Looking at our t-Test above, we see the mean for the Male variable is higher, which suggests men spend more on tech than women.
