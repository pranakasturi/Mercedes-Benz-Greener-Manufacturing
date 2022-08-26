# Mercedes-Benz-Greener-Manufacturing

<b>Description:</b>

Mercedes-Benz is the leader in the premium car industry. With a huge selection of features and options, customers can choose the customized Mercedes-Benz of their dreams.
To ensure the safety and reliability of every unique car configuration before they hit the road, the company’s engineers have developed a robust testing system. As one of the world’s biggest manufacturers of premium cars, safety and efficiency are paramount on Mercedes-Benz’s production lines. However, optimizing the speed of their testing system for many possible feature combinations is complex and time-consuming without a powerful algorithmic approach.

Using this Machine Learning model we can reduce the time that cars spend on the test bench. 

<b>Model building:</b>

1.	First I have imported different python libraries (NumPy, Pandas, matplotlib, scikit-learn, seaborn).
2.	Then Imported data in python environment.
3.	Next analyzed data and dropped unwanted ID column and target column.
4.	Used label encoder to transform few columns.
5.	Ran test on data to check variance value.
6.	After test found 12 variables whose variance value is equal to zero, so had to drop those variables for further analysis.
7.	Now, done some data cleaning on data by checking null and unique values.
8.	Performed dimensionality reduction using PCA(Principal Component analysis).
9.	Used XGBoost  to predict values.
10.	Computed RMSE (Root Mean Square Error) on model.
11.	Plotted distplot to compare target and predicted values.
12.	Now using test data file again checked the RMSE value on data, also plotted graph for same to analyze model accuracy.
