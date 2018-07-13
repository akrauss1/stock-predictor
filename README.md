# stock-predictor
A stock predictor using quandl to get data and facebook's prophet time series model- I think it's pretty cool.

Document your research and analysis including a summary, an explanation of your modeling approach as well as the strengths and weaknesses of any variables in the process. You should provide insight into your analysis, using best practices like cross validation or applicable prediction metrics.

Technical Analysis- 

In my model, I captured my data using quandl, and ran each stock objects through a series of transformation functions in the Stock class to prepare it for fitting. I fit it with Facebook's open source Prophet model. I chose Prophet because Prophet handles gaps in dates, trends and outliers very well, accounts for daily, weekly, and yearly seasonality, and accounts for holidays in particular when training and forecasting. I used the results plot some visuals, including an 80% range, and how frequently the stock correctly rose or fell compared to the predictions.

Stock prediction in itself is flawed when using just historical stock data to make predictions, for several reasons. First, it doesn't account for the "randomness" of new information about a company that undoubtedly effects the value, or even percieved value, of the company, hence the value of the stock. Second, stock isn't necessarily as cyclical as, say, sales of a store throughout the year. While it may experience peaks and troughs, they aren't very predictable, as they are not "seasonal" like sales may be. Finally, the rate of change of a stock isn't predictable, and as we move forward some days and rolling testing data becomes training data, the model may struggle to recover and it may take several days or longer for its predictions to land within an "acceptable" selected confidence interval. 


