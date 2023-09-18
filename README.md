# Price-of-diamonds

The purpose of this investigation was to examine the connection between price and a range of diamond characteristics. To accomplish this, we employed a dataset sourced from the Blue Nile website, which encompasses details regarding over 1,200 diamonds, including their associated prices. The attributes under scrutiny in this study are carat weight, clarity, color, and cut, collectively referred to as the 4Cs. The dataset used for this report includes 1214 recordings of diamonds including carat, clarity, color, cut, and price. The dataset is available on the Blue Nile website. We ran a simple validation test to check for quality and confirmed that there are no signs of null values or invalid characters that could potentially provide misleading results over the course of the analysis.

# Relationships between variables

- Carat vs. color
  ![image](https://github.com/ambroso0/Price-of-diamonds/assets/38117605/c912b75f-1782-4f36-858b-5810779db259)

The boxplot above represents the relationship between color and carat — noting here that the y-axis represents the log of carat for more visible boxplots. There is no immediately apparent trend or pattern between the two properties, though it is interesting to note that color I has many more outliers than the other categories.

- Clarity vs. color
  ![image](https://github.com/ambroso0/Price-of-diamonds/assets/38117605/3ec30464-d22b-4c19-bc6e-2bf704b5ac5a)

The stacked chart above shows the proportions and relationship between clarity and color. For most of the clarity categories, color is relatively evenly distributed, with no immediately apparent trends. However, the FL clarity only has D- and F-colored diamonds. If this were due to some external factor, such as the conditions each diamond was created in, we might expect a trend. Therefore, the FL category may be different from the others because it has relatively few diamonds. Consumers may believe, however, that a flawless diamond is more often a higher-quality color diamond as well because high quality in one property can be associated with high quality in another.

# Simple linear regression
![image](https://github.com/ambroso0/Price-of-diamonds/assets/38117605/11a649c0-e73f-4cce-a5a8-e5733425db7b)

From this scatterplot, we notice a positive correlation between a diamond’s price and its carat size, with an increase in the price of the diamond in response to an increase in the carat value. However, in this initial plot, the data points are not equally distributed on both sides of the regression line, and the relationship between the variables does not appear linear. The vertical spread of the data point is not constant and the assumption that the relationship is linear may not be met. The assumptions that variance for the error term is constant and that the error mean is 0 are also not met. We proceed with plotting residuals to investigate how well the regression model fits the data and to check the linear regression assumptions more closely. 

![image](https://github.com/ambroso0/Price-of-diamonds/assets/38117605/e1e6d7fe-9f0d-40a0-864d-da1d165defaa)

The residual plot shows a curved pattern with non-constant variance, and the variance increases for higher-fitted y values. Just as the first scatterplot shows, the residuals are not evenly scattered on both sides of the horizontal axis. The majority of the points are located underneath the regression line. The vertical spread, or variance for the error term, is not constant. In this instance, we would consider a transformation of the response variable. In order to determine the type of transformation that better suits the model, we will run a Box-Cox analysis. 

![image](https://github.com/ambroso0/Price-of-diamonds/assets/38117605/6d7a401d-9203-4d34-a0d0-ebe46fafb114)

This graph of the transformed predictor and response variables shows a linear relationship, indicating that the transformations were successful.

*code will be provided upon request.
