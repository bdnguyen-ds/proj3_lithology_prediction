# Lithology prediction from oil and gas well log data
The aim of this project is to use supervised logistic regression and other classification methods to train and ultimately predict the rock types present in a zone-of-interest for unknown (unlabeled) wells.

### Lithology prediction addresses a crucial part of a potential investment into exploring for oil and gas:
- How economical is this field likely to be based on its predicted size? So we could imagine that mis-predictions for the overall thickness of certain lithologies could have very significant consequences in the risk aversion for an oil and gas investment portfolio. In other words, if the size of the prize is not likely to deliver enough return-on-investment, that project would likely not get funded.
- On the flipside, if a company has already committed to drilling wells and they subsequently find out there was a lot less reservoir than previously predicted, then the value of that project could become severely eroded.


### Features, and Target Variables
- The targets here are 9 identified rock types (Sandstone, Fine Siltstone, Coarse Siltstone, Marine Silty Shale, Mudstone, Wackestone, Dolomite, Packstone, and Bafflestone)
- The features consist of 5 numerical and 2 categorical features. 
  - Numerical features are down-hole measurements recorded from these tools: Gamma Ray, Deep Resistivity, differential Porosity (calculated), Neutron-Density Porosity, and Photoelectric.
  - Two categorical features made available are: Marine or Non-Marine nature of the lithology encountered, and RelativePosition between one lithology type and another (i.e., some lithology types will never be adjacent)

### Datasets and Tools
- The dataset containing the predictor and target variables comes from the first-every machine learning contest, hosted by The Leading Edge magazine, using well log data in 2016: https://github.com/seg/2016-ml-contest/blob/master/index.ipynb)
- Tools and modules include: Bokeh for interactive visualization, scikit-learn (LogReg,KNN,RF,DT,GBT,XGBoost), PCA, Self-Organizing Maps (SuSi SOM), Matplotlib/Seaborn
