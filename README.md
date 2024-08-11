# ML-Model-to-predict-used-car-prices
This project aims to predict the used car prices in USA. 

**Preliminary Analysis of Dataset**
The dataset has approximately 4300 records from 1969 to 2021. Of these records few of them contained unstructured bad data which needs to be cleaned. There is a potential dependent variable in the dataset (Price) which we predict. On the other side, we have few predictor variables which supports our prediction. To give broad view of the explanatory variables – The Brand variable describes the brand of a car (e.g., Audi, BMW etc.). The Body variable describes the type of a body that the car has. It can be crossover, hatch, van, sedan etc., Similarly the Engine Type variables has four possible values like petrol, diesel, gas and other. The Mileage variable gives the individual mileage of a car and the Engine version describes the version of the engine that the car has. By considering all these predictors, we estimate the respective price of a car.

The dataset used for the project is that of used car sales data containing various columns like: Brand of a car, Price, Body type of a car, Mileage, Engine Version, Engine Type, Is Registration, Manufacturing Year. 
As the aim is to predict the price of used cars in USA taken into account the various other variables.

**Dependent variable:** Price of a car ( measured in $)

**Independent Variables:**
•	Brand of a car – The various Brands of a car like BMW, Audi, Toyota etc.,
•	Body type – The type of body by which the motor vehicle is named like sedan, crossover etc.,
•	Mileage – The Mileage of a car in number.
•	Engine Version – Contains the Engine version of a car.
•	Engine Type – Contains the type of the engine( Petrol/Diesel/Gas).
•	Is Registration – Shows whether the car is registered or not.
•	Manufacturing Year – Contains the year of manufacturing of the vehicle. Typically ranging from 1969 to 2016.

**Data Cleaning**
The dataset considered was in an unstructured format and had lots of bad data which made the regression analysis not to move forward. So, this data had to be cleaned to make it feasible for regression. The removal of the unusual observations from the dataset was done to make the dataset structured.
Apart from this, it also had predictor variables which have categorical values in it. And even doesn’t support the regression analysis. In order to handle this, I have created respective dummy variables for the predictor variables to use them for the price prediction.

This is how the structured dataset looks like after cleaning –

<img width="474" alt="image" src="https://github.com/user-attachments/assets/0ff63778-0e10-484f-b7eb-4cb38eaa43fb">


**Exploratory Data Analysis**
By visualizing the data, we can know how the data is distributed, find patterns and then we can summarize and draw conclusions which helps the business grow.
Following are the conclusions that are found using descriptive analytics –

<img width="471" alt="image" src="https://github.com/user-attachments/assets/a20df607-2d0f-4262-a3c3-71c5e1a8af23">

From the above chart, we can find the highest and lowest priced branded car. And each brand has its respective body types, we can find the individual price of each body type for each individual brand. For example, Mercedes – Benz Crossover is the highest priced brand from the entire dataset and Mitsubishi Van is the lowest of all.
Also, a deep analysis over the chart helps us to draw few other meaningful conclusions. Like the crossover body type for each brand seems to have highest price when compared with other body types. But there’s also an exceptional scenario which is Renault brand, where the van body type picks the highest cost of all other body types. The sedan is the second highest priced car. The hatchback is the least priced car in the different body types available due to its compact size and less features available on the vehicle. In the premium cars the Toyota is the highest priced car compared to Renault and Mitsubishi.
Following is the chart which describes the price based on Engine Type –

<img width="478" alt="image" src="https://github.com/user-attachments/assets/005b5c15-7b03-4460-b29e-05a177fe880c">

We can see that, the car which has an Engine Type as Diesel makes the highest price. And the lowest goes to other engine type. Apart from that, the registered cars will have higher prices than unregistered cars from the above chart. The other engine type and the gas engine type cost less compared to the diesel and petrol engine type due to its low popularity among the customers as most of the customers might prefer diesel or petrol cars compared to other engine types. And of course, these conclusions and finding makes some sense and adds value to the model.

**Regression Model**

Regression Analysis Technique is a set of statistical processes which is used for estimating the relationships between dependent and one or more independent variables. I have used Linear Regression Technique which establishes a relation among two types of variables (dependent & independent) where we have more than one explanatory variables. Linear regression is the best suited regression to analyse the given data set. The main purpose of selecting linear regression if the independent variables are successful in predicting the dependent variable and which independent variables are statistically significant or not. The variables that are used in the linear regression to estimate the price of a used car are as follows

**Dependent Variable** – Price.
**Independent Variables** – Brand, Body, Mileage, Engine Type, Engine Version, Is
Registration.
As discussed above, since few of the predictor variables has categorical data, The dummy variables need to be created in order to include them in the regression analysis.
Following figure shows the respective dummy variables for each independent variable –

<img width="326" alt="image" src="https://github.com/user-attachments/assets/d99f2270-e4ae-416a-a553-d495591a0098">

<img width="330" alt="image" src="https://github.com/user-attachments/assets/686bf7e2-d101-4cda-a403-5e5d0fce0ae5">


As the dummy variables are created, Next step is to apply linear regression using all the independent variables including the dummies that we have created. The software that is used to apply the regression is IBM SPSS. The software enables us to select the variables which are dependent and independent and gives a regression result.


**RESULTS**
The linear Regression analysis on the car price dataset gives a result which are shown below 

<img width="430" alt="image" src="https://github.com/user-attachments/assets/2eac4253-953a-408e-b527-e2109b6df128">

The above summary of the linear regression model. The value of R square is 0.42 which means the above model is only 42% accurate. The independent variables are 42% successful in predicting the price of a used car. 

<img width="435" alt="image" src="https://github.com/user-attachments/assets/a06b3122-a7a7-4adc-8ad9-d5b5e35bdcd4">

The above figures show the regression coefficients of each independent variable. There are positive coefficients and negative coefficients. The positive coefficients will have positive impact on predicting the car price which means if the coefficient value increases, the price (dependent variables) also increases. The negative coefficients do the vice versa. Also, the positive coefficients such as “engine version”, “Brand BMW” will give better price but they are not statistically significant because their p-values are greater 0.05. The variables whose p- values are greater than 0.05 are not considered as significant variables. Additionally, the variables which have negative coefficients are almost statistically significant because the p values being less than 0.01.

So, the Regression Equation be like –
Y = 55146.70 + 167.567 * X EngineVersion – 107.811 * X Mileage + 1893.531 * X BrandBMW + 10366.839 * X BrandMercedesBenz – 15478.519 * X BrandMitsubishi – 13312.277 * X BrandRenault – 6595.915 * X BrandToyota – 6954.763 * X BrandVolkswagen – 20560.822 * X BodyHatch – 12081.589 * X BodyOther – 15726.191 * X BodySedan – 15765.098 * X BodyVagon – 16874.133 * X BodyVan – 6672.785 * X EngineGas – 4614.502 * EngineOther – 3295.537 * X EnginePetrol – 9631.756 * X RegistrationNo

**Interpretation of R- Square**
The model’s R- Square value is 0.420 which is lower and not as a very good prediction. It simply means that the predictor variables can explain 42% of the variance alone. In order to increase the R- Square for the model, we need a high-level dataset which contains few more explanatory variables which helps us in prediction of a price.

**Results drawn from regression coefficients**
Brand BMW costs $1893.531 more than Audi.
Brand Mercedes-Benz costs $10366.839 more than Audi. And this is the highest priced branded car from entire dataset.
Brand Mitsubishi costs $15478.519 lower than Audi. This is the lowest priced car. Brand Renault costs $13312.277 lower when compared with Audi.
Brand Toyota costs $6595.915 lower than Audi. And Brand Volkswagen costs $6954.763 lesser than Audi.
In a similar way,
The Body Hatch costs $20560.822 lesser than crossover.
Body Sedan costs $15726.191 lesser when compared with crossover. And Body Type Vagon costs $15675.998 lesser than crossover. Similarly, Van costs $16874.133 lower than Crossover.
For Engine Types,
The Cars which have an Engine Type of ‘Diesel’ has the highest price and ‘Petrol’ has the next highest price.
We can also conclude that, Registered cars have more prices when compared with unregistered cars, which suits a real-world scenario too.
Additionally, A project that we looked which conducted regression on Ford cars. The same linear regression was used in the project. The linear regression gave a R square value of 84% which is almost double the value of the above model. After spending a great amount of time on the ford cars project, we realized that the independent variables such as Miles travelled, Miles per Gallon, Model year were very good independent variables in terms of statistical significance. These variables give the better price prediction of a used car and can help a car dealer to find the accurate price of the car.

**Model Evaluation**
For evaluating a regression model, we have few metrics of evaluation based on outliers. They describe how well the model performed. The evaluation metrics we have are –
**Mean Absolute Error (MAE)** – The mean of absolute value of errors.

<img width="77" alt="image" src="https://github.com/user-attachments/assets/f761c721-6be6-4c10-a957-6683b6a2817f">

**Mean Square Error (MSE)** – The mean of squared errors.

<img width="84" alt="image" src="https://github.com/user-attachments/assets/808a5fbc-d9b4-4301-bfac-637d8b150760">

**Root Mean Square Error (RMSE**) – The square root of mean of squared errors. We calculate RMSE if we consider all the outliers in our dataset.

<img width="115" alt="image" src="https://github.com/user-attachments/assets/f6dfe785-581d-4c55-8ff3-ff1f1f004a60">

Where – yi = Predicted value yi^ = Actual value

**PRESCRIPTIVE ANALYTICS**

Prescriptive Analytics tells us what should be done as preventive measure based on past historical data. This suggests business persons, executives, managers and manufactures to take right decisions in order to achieve better results. As this is the complex step of Business, this requires more specialized knowledge to make predictions or to offer recommendations.

**Prescriptive Analytics based on the Findings**
Of all the branded cars with its respective body types, the cars with body type of Crossover are the high priced. And the second highest goes for the cars with body type Sedan. But there’s an exceptional case with Renault where van and vagon have highest prices than crossover and sedan. The lowest priced cars were in Mitsubishi brand. This gives a clear picture to a car dealer which type of car can be sold at a better price for increasing the revenue.


Another consideration that needs to be made is how to examine and analyse the growing market in used cars. As it’s a great liability for the mankind, the prices get varied according to the day- to-day basis based on real world situations like seasons, recessions, availability, special editions etc., For example, if a recession occurs then the sales will be greatly decreased which also affects the prices of the vehicles, because of which we see more fluctuations happening all around.

<img width="270" alt="image" src="https://github.com/user-attachments/assets/14b9a901-32c8-4ff7-90b1-e741907b0b3e">

From the above figure, as preventive measures we need to consider the sales of the cars for each year and predict the price of the used car.


**CONCLUSION**
To conclude the model based on the above regression, we can say that the model is somewhat weak because of the low R - square value. The independent variables do not clearly signify the price of the car. Furthermore, the better price of a used car can be predicted when few more variables are considered in regression. Although the regression techniques that were applied on this dataset were precise, still the expected outcome was difficult to obtain which makes the regression model as a weak model to predict the price of a used car.
Since the linear regression allows us to estimate how a dependent variable change based on our given predictor variables, in order to increase the R – square value, we just need a higher level of dataset and few more explanatory variables which supports the dependent variable in its prediction.
Thus by a well understanding and analysis of using descriptive and regression techniques, the prediction of price is performed.




















