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













