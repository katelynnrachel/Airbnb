# Airbnb Analysis

<img width="333" alt="Screen Shot 2022-12-15 at 10 32 51 AM" src="https://user-images.githubusercontent.com/107594280/207939987-69d7306b-7537-44f6-90ab-aab7f0a1dc21.png">


## Background and Overview
Airbnb have gained traction as people want a personalized and private vacation experience. As someone who has frequently utilized Airbnb with friends and family, I was interested in the data and trends surrounding the program. I've conducted analysis on Airbnb data from Los Angeles in 2021, to answer questions about the business. In addition, as a resident of Los Angeles myself, I'm interested in what the market looks like and could use this information to potentially invest in Airbnb properties.

#### Questions to Answer
1. How do variables such as location, the number of bedrooms offered, and the minimun allowed nunber of nights affect the price?
2. Can we use those variables to predict what the price of an Airbnb should be?
3. Which room type is the most offered?
4. What is the average number minimum nights across Airbnbs? maximum?
5. What is the average price per room?

## Data Exploration + Analysis
At first I was unsure what topic I wanted to tackle for the project. I searched for interesting datasets on google and Kaggle, and would start cleaning a few of them as well until I realized that it didn't offer me the information I ultimately needed. In the end, I used data from [Inside Airbnb](http://insideairbnb.com/get-the-data/) which contained the necessary information to conduct my analysis. After cleaning the dataset on pandas and filtering out unnecessary columns, I could then conduct my machine learning analysis. I also used Tableau to create visuals to better understand the overall data.


## Visualizations + Results
### Background
<img width="230" alt="Screen Shot 2022-12-12 at 6 02 27 AM" src="https://user-images.githubusercontent.com/107594280/207064604-e56be070-dee8-4aab-912a-84929be6afed.png">
<img width="350" alt="Screen Shot 2022-12-12 at 5 59 38 AM" src="https://user-images.githubusercontent.com/107594280/207063989-d19d9e92-f60d-4d32-901f-e02079f1835d.png">
 <img width="550" alt="Screen Shot 2022-12-12 at 6 05 45 AM" src="https://user-images.githubusercontent.com/107594280/207065362-5ee55637-ec25-4d07-af68-a1a35dfc60b6.png">
 
 - First, I wanted to know how many listings were in my dataset, and what were the types of rooms offered to users. Here we can see that an entire home/apt is the most popular type of listing.
 - I also created a map to learn where in Los Angeles there are a greater amount of listings and how dense each area is.
 
 ### Summary Statistics
 <img width="265" alt="Screen Shot 2022-12-12 at 6 16 00 AM" src="https://user-images.githubusercontent.com/107594280/207067804-5e669fd5-23ab-469e-bc96-0d044842f630.png"><img width="335" alt="Screen Shot 2022-12-12 at 6 16 33 AM" src="https://user-images.githubusercontent.com/107594280/207067923-ea0b6547-74d8-4ba5-b3a7-84f8378e007a.png"><img width="348" alt="Screen Shot 2022-12-12 at 6 16 13 AM" src="https://user-images.githubusercontent.com/107594280/207067857-f0c08db3-c983-4847-8b76-a5c76be2875f.png">

## Machine Learning
I decided to use a DecisionTreeRegressor model to see if features such as latitude, longitude, accommodates, bedrooms, number of beds, minimum_nights, maximum_nights, number_of_reviews, review_scores_rating could predict the price of a listing. Decision Trees pose many benefits over other models in that it is a simpler and quick way to conduct classification or regression problems. However, the model is also prone to "overfitting" which can increase error. It is also harder to use with continuous variables and can be sensitive to changes.

## Machine Learning Results
<img width="304" alt="Screen Shot 2022-12-12 at 7 13 51 AM" src="https://user-images.githubusercontent.com/107594280/207081550-2706cfff-d78c-4c61-af91-4d246fe0c8e4.png">

- Here we see that the model received an r-square of 0.99. This score indicates that the model may be a good fit and that the regression model fits the observed data.


<img width="304" alt="Screen Shot 2022-12-12 at 7 20 06 AM" src="https://user-images.githubusercontent.com/107594280/207082997-948483f9-adb5-45dd-9f30-e529abc6ee7b.png">

- We can also look at the Mean Squared Error (MSE) and Root Mean Squared Error (RMSE) as indictors of how well the model performs. However, both the zmsze and RMSE are very high, meaning it is unlikely that the model accurately predicts the reponse.

<img width="494" alt="Screen Shot 2022-12-12 at 7 26 06 AM" src="https://user-images.githubusercontent.com/107594280/207084469-3376e1ae-7700-4969-94d5-648c093b58f5.png">

- Furthermore, this graph also shows the disparity between the model and the correct data.

## Summary and Future Use
As we can see, this model was not helpful in predicting accurate data. In the future, with more time, I would like to run other machine learning models such as a Random Forrest algorithm to test the model again which will work against any "weak learners."  I would also like to include categorical data from the data source by converting them into dummy variables. 

