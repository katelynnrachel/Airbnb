# Airbnb

## Background and Overview
Airbnb have gained traction as people want a personalized and private vacation experience. As someone who has frequently utilized Airbnb with friends and family, I was interested in the data and trends surrounding the program. I've conducted analysis on Airbnb data from Los Angeles in 2021 to answer questions about the business.

#### Questions to Answer
1. How do variables such as location, the number of bedrooms offered, and the minimun allowed nunber of nights affect the price?*
2. Which room type is the most offered?
3. What is the average number minimum nights across Airbnbs? maximum?
4. What is the average price per room?


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
I decided to use a DecisionTreeRegressor model to see if features such as latitude, longitude, accommodates, bedrooms, number of beds, minimum_nights, maximum_nights, number_of_reviews, review_scores_rating could predict the price of a listing.

## Machine Learning Results
<img width="304" alt="Screen Shot 2022-12-12 at 7 13 51 AM" src="https://user-images.githubusercontent.com/107594280/207081550-2706cfff-d78c-4c61-af91-4d246fe0c8e4.png">

- Here we see that the model received an r-square of 0.99. This score indicates that the model may be a good fit and that the regression model fits the observed data.


<img width="304" alt="Screen Shot 2022-12-12 at 7 20 06 AM" src="https://user-images.githubusercontent.com/107594280/207082997-948483f9-adb5-45dd-9f30-e529abc6ee7b.png">

- We can also look at the Mean Squared Error (MSE) and Root Mean Squared Error (RMSE) as indictors of how well the model performs. However, both the zmsze and RMSE are very high, meaning it is unlikely that the model accurately predicts the reponse.

<img width="494" alt="Screen Shot 2022-12-12 at 7 26 06 AM" src="https://user-images.githubusercontent.com/107594280/207084469-3376e1ae-7700-4969-94d5-648c093b58f5.png">

- Furthermore, this graph also shows the disparity between the model and the correct data.

## Summary and Future Use
In the future, I would like to determine whether there is a differeht model that could better suit my needs for predicting the Airbnb data. Throughout the process, I had attempted to run different models such as a logistic regression or classification model, but ultimately decided to run the decision tree. I would also like to include categorical data from the data source by converting them into dummy variables. 

