# ML-Model-to-predict-used-car-prices
This project aims to predict the used car prices in USA. 

**Preliminary Analysis of Dataset**
The dataset has approximately 4300 records from 1969 to 2021. Of these records few of them contained unstructured bad data which needs to be cleaned. There is a potential dependent variable in the dataset (Price) which we predict. On the other side, we have few predictor variables which supports our prediction. To give broad view of the explanatory variables – The Brand variable describes the brand of a car (e.g., Audi, BMW etc.). The Body variable describes the type of a body that the car has. It can be crossover, hatch, van, sedan etc., Similarly the Engine Type variables has four possible values like petrol, diesel, gas and other. The Mileage variable gives the individual mileage of a car and the Engine version describes the version of the engine that the car has. By considering all these predictors, we estimate the respective price of a car.

The dataset used for the project is that of used car sales data containing various columns like: Brand of a car, Price, Body type of a car, Mileage, Engine Version, Engine Type, Is Registration, Manufacturing Year. 
As the aim is to predict the price of used cars in USA taken into account the various other variables.
**Dependent variable:** Price of a car ( measured in $)
**Independent Variables: ** 
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

This is how the structured dataset looks –







