# House-prices-Baton-Rouge-multiregression-
This project analyzes 1,080 house sales in Baton Rouge using linear regression. It estimates the effect of house size and age on price, tests individual and joint significance, explores interaction effects, and computes confidence intervals for price predictions based on age and size.
library(ggplot2)

houses<read.csv("/Users/test/Library/Containers/com.microsoft.Excel/Data/Downloads/br2.csv", sep= ",")
print(houses)
model6<-  lm(price ~ sqft + bedrooms + baths + age + owner + pool + traditional + fireplace + waterfront, data = houses)
summary(model6)

#sqft (β1): For each additional square foot increase, we expect, on average, an increase of β1 in house price, holding other variables constant.
#bedrooms (β2): For each additional bedroom, we expect, on average, an increase of β2 in house price, holding other variables constant.

model7<-lm(log(price/1000) ~ sqft + bedrooms + baths + age + I(age^2) + owner + pool + traditional + fireplace + waterfront, data = houses)
summary(model7)
![Rplot01](https://github.com/user-attachments/assets/d64677d6-4961-4fd7-b9ce-b03d91a02f6c)
