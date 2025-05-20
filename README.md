# House-prices-Baton-Rouge-multiregression-
This project analyzes 1,080 house sales in Baton Rouge using linear regression. It estimates the effect of house size and age on price, tests individual and joint significance, explores interaction effects, and computes confidence intervals for price predictions based on age and size.
library(ggplot2)

ggplot(hsold, aes(x = sqft, y = price)) +
  geom_point(alpha = 0.5, color = "steelblue") +
  geom_smooth(method = "lm", formula = y ~ x + hsold$age, color = "darkred") +
  labs(title = "House Price vs Square Footage (Controlling for Age)",
       x = "Size (sqft)",
       y = "Price (USD)") +
  theme_minimal()

ggplot(hsold, aes(x = age, y = price)) +
  geom_point(alpha = 0.5, color = "orange") +
  geom_smooth(method = "lm", formula = y ~ x + hsold$sqft, color = "darkgreen") +
  labs(title = "House Price vs Age (Controlling for Size)",
       x = "Age (years)",
       y = "Price (USD)") +
  theme_minimal()

### 🏠 House Price vs Square Footage
![Price vs Sqft](visualizations/price_vs_sqft.png)

### 🕒 House Price vs Age
![Price vs Age](visualizations/price_vs_age.png)
