# Final-Capstone-Time-Series-Neural-Network

While ARIMA and neural networks machine learning techniques have proven to be quite successful in predicting the stock market, 
applying them to the more volatile prices of cryptocurrencies may be more challenging given that cryptocurrencies don’t have 
indexes or indicators like stocks. The project will work to predict the price of Ethereum (ETH) using daily realtime trading features, 
such as close price, high price, open price, etc., and more global features such as google searches per day, the price of Bitcoin, 
the values of the US dollar and Euro, and the number of active addresses that may serve as a sort of index for price prediction. 
The goal is to give a clear indication as to when to buy and sell Ethereum to maximize one’s return.

While the deep learning model deploying an RNN network worked well to predict the daily price of Ethereum, all efforts to tune hyperparameters and the model were not quite able to beat the ARIMA model.

Both models show nearly zero centered histograms of their residuals and there is no clear trend. The intent of the deep learning RNN model was to help explain the areas of higher volitility shown in the ARIMA model. This is the biggest area of improvement that I see. Having tuned the RNN model as best as possible, it seems clear that to utterly outperform the ARIMA model, different or additional non-time series features are needed to explain the highly volitile nature of Ethereum cryptocurrency.

This is not to say that this project was not successful! The ARIMA model showing a MAPE of 2.88% (as compared to ~3+/-1.5% achieved with the RNN above - note MAPE is used because the scales of data are different) is still a solid deliverable. Assuming an investor knows his or her cost basis of currently owned Ethereum - i.e. how much was originally invested - this percent error can be reasonably built in as a sort of buffer for the next days choice of what to buy or sell.

In a production environment, this ARIMA model can be continuously updated daily and have it's p, d, and q adjusted as needed in the same way shown in this notebook. With a given cost basis and known mean average error (here, 8.8) that can be used as buffer to ensure a successful, profitable transactions, the next days prediction can be used to provide recommendations to either hold, sell, or buy additional Ethereum.
