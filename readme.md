## 👨‍💻 Built with
![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)

##  Descripction
Data used in this project: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection)

The CSV file contains over 5000 text messages.

File contain columns:
```bash
model	year	price	transmission	mileage	
fuel type	engine size	mileage2	fuel type2	
engine size2	reference
```

This project is about Data cleansing, data visualisation and also using sklearn ML model to predict price of car.

- **To handle with collected data I used Jupyter Notebook with libraries:**
    - pandas
    - matplotlib
    - seaborn
    - sklearn


##  📊Data cleansing, visualisation and price prediction with ML model:

**Data cleansing part**
- Collected data in CSV has:
    - repeated columns (with missing values): 
      - mileage and mileage2;
      - engine size and engine size2;
      - fuel type and fuel type2;
    - values in string - converted to numeric;
      - price;
      - mileage;
      - year;
      - engine;
      
**Data visualisation part**
- boxplot to visualise spread of variable price;
- histogram - distribution of the value price;
- boxplot to visualise spread of mileage;
- histogram - distribution of the mileage;
- heatmap to check the correlations;
- scatterplots with price vs. mileage, mileage vs. year, price vs. year;
- histogram with numbers of oferts depending on fuel type and boxplot Price vs Fuel;
- histogram with numbers of oferts depending on transmission system and boxplot Price vs transmission;
- histogram with numbers of oferts depending on engine size and boxplot Price vs engine size;
- histogram with numbers of oferts depending on year of production and boxplot Price vs year of production;

**ML price prediction part**

Using a sklearn model to predict price, used regressions: polynominal and linear.

When we look at the scores of each prediction, we will se that the best was polynomynal regression with degree 3.

The best score which was achieved - polynominal regression on degree 3 with 5 independent values: 

'year', 'engine size', 'mileage', 'transmission', 'fuel type'

**Score of testing is: 91.94%**
