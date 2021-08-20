# reddit-sentiment-analysis
This program goes thru reddit, finds the most mentioned tickers and uses Vader SentimentIntensityAnalyzer to calculate the ticker compound value.  

## Program Parameters
<pre>
subs = []           sub-reddit to search
post_flairs = {}    posts flairs to search || None flair is automatically considered
goodAuth = {}       authors whom comments are allowed more than once
uniqueCmt = True    allow one comment per author per symbol
ignoreAuthP = {}    authors to ignore for posts
ignoreAuthC = {}    authors to ignore for comment 
upvoteRatio = float upvote ratio for post to be considered, 0.70 = 70%
ups = int           define # of upvotes, post is considered if upvotes exceed this #
limit = int         define the limit, comments 'replace more' limit
upvotes = int       define # of upvotes, comment is considered if upvotes exceed this #
picks = int         define # of picks here, prints as "Top ## picks are:"
picks_ayz = int     define # of picks for sentiment analysis
</pre>

# How to run:
    
    pip install -r requirements.txt
    python3 reddit-sentiment-analysis.py
    
    
## Sample Output
It took 33.01 seconds to analyze 2087 comments in 22 posts in 2 subreddits.

Posts analyzed saved in titles

5 most mentioned tickers: 
BABA: 27
NVDA: 10
PLTR: 9
TSLA: 8
GME: 8
[*********************100%***********************]  1 of 1 completed
Linear result :                  Real  Predictions Real Buy/Sell Predict Buy/Sell  Model test
Date                                                                          
2021-08-17  182.710007   184.148243          Sell             Sell           1
2021-08-18  173.729996   183.142156          Sell             Sell           1
Linear prediction :[184.14824323 183.14215573]
linear result :Date
2021-08-17    182.710007
2021-08-18    173.729996
Name: Prediction_close, dtype: float64
Linear regression score:-140769009.4096502, r2_lr:-1.2484277941729451, mse_lr=45.328640085198984
Decision Tree :                  Real  Predictions Real Buy/Sell Predict Buy/Sell  Model test
Date                                                                          
2021-08-17  182.710007   188.619995          Sell             Sell           1
2021-08-18  173.729996   188.619995          Sell             Sell           1
Decision Tree prediction : [188.61999512 188.61999512]
Decision Tree result :Date
2021-08-17    182.710007
2021-08-18    173.729996
Name: Prediction_close, dtype: float64
Desicon Tree :-0.3722050011272662, r2:-5.365033328063655, mse = 128.3200223755557
[*********************100%***********************]  1 of 1 completed
Linear result :                  Real  Predictions Real Buy/Sell Predict Buy/Sell  Model test
Date                                                                          
2021-08-17  199.500000   206.278453          Sell             Sell           1
2021-08-18  194.580002   208.792723          Sell             Sell           1
Linear prediction :[206.27845288 208.79272326]
linear result :Date
2021-08-17    199.500000
2021-08-18    194.580002
Name: Prediction_close, dtype: float64
Linear regression score:-178490875.0281496, r2_lr:-19.48623987524777, mse_lr=123.9744369509597
Decision Tree :                  Real  Predictions Real Buy/Sell Predict Buy/Sell  Model test
Date                                                                          
2021-08-17  199.500000   201.880005          Sell             Sell           1
2021-08-18  194.580002   201.880005          Sell             Sell           1
Decision Tree prediction : [201.88000488 201.88000488]
Decision Tree result :Date
2021-08-17    199.500000
2021-08-18    194.580002
Name: Prediction_close, dtype: float64
Desicon Tree :-1.1177472969046716, r2:-3.8709854980135363, mse = 29.47723389894236
[*********************100%***********************]  1 of 1 completed
Linear result :                 Real  Predictions Real Buy/Sell Predict Buy/Sell  Model test
Date                                                                         
2021-08-17  24.500000    24.936312          Sell             Sell           1
2021-08-18  23.969999    24.798804          Sell             Sell           1
Linear prediction :[24.93631224 24.7988037 ]
linear result :Date
2021-08-17    24.500000
2021-08-18    23.969999
Name: Prediction_close, dtype: float64
Linear regression score:-680506.1111998325, r2_lr:-5.246228672412619, mse_lr=0.43864254509129996
Decision Tree :                 Real  Predictions Real Buy/Sell Predict Buy/Sell  Model test
Date                                                                         
2021-08-17  24.500000    24.900000          Sell             Sell           1
2021-08-18  23.969999    24.889999          Sell             Sell           1
Decision Tree prediction : [24.89999962 24.88999939]
Decision Tree result :Date
2021-08-17    24.500000
2021-08-18    23.969999
Name: Prediction_close, dtype: float64
Desicon Tree :-0.7469181519206576, r2:-6.1655195978103485, mse = 0.5031999176026147
[*********************100%***********************]  1 of 1 completed
Linear result :                  Real  Predictions Real Buy/Sell Predict Buy/Sell  Model test
Date                                                                          
2021-08-17  686.169983   713.879597          Sell             Sell           1
2021-08-18  665.710022   717.685857          Sell             Sell           1
Linear prediction :[713.8795972  717.68585718]
linear result :Date
2021-08-17    686.169983
2021-08-18    665.710022
Name: Prediction_close, dtype: float64
Linear regression score:-585227436.9823601, r2_lr:-15.575381175938546, mse_lr=1734.65508499599
Decision Tree :                  Real  Predictions Real Buy/Sell Predict Buy/Sell  Model test
Date                                                                          
2021-08-17  686.169983   717.169983          Sell             Sell           1
2021-08-18  665.710022   717.169983          Sell             Sell           1
Decision Tree prediction : [717.16998291 717.16998291]
Decision Tree result :Date
2021-08-17    686.169983
2021-08-18    665.710022
Name: Prediction_close, dtype: float64
Desicon Tree :-0.6880698957115081, r2:-16.24338915078222, mse = 1804.563789844513
[*********************100%***********************]  1 of 1 completed
Linear result :                  Real  Predictions Real Buy/Sell Predict Buy/Sell  Model test
Date                                                                          
2021-08-17  163.929993   162.628876          Sell             Sell           1
2021-08-18  163.550003   162.557930          Sell             Sell           1
Linear prediction :[162.62887606 162.55793034]
linear result :Date
2021-08-17    163.929993
2021-08-18    163.550003
Name: Prediction_close, dtype: float64
Linear regression score:-75476916.63317892, r2_lr:-36.08114865947168, mse_lr=1.3385563645103888
Decision Tree :                  Real  Predictions Real Buy/Sell Predict Buy/Sell  Model test
Date                                                                          
2021-08-17  163.929993   162.520004          Sell             Sell           1
2021-08-18  163.550003   162.520004          Sell             Sell           1
Decision Tree prediction : [162.52000427 162.52000427]
Decision Tree result :Date
2021-08-17    163.929993
2021-08-18    163.550003
Name: Prediction_close, dtype: float64
Desicon Tree :-0.7036638484107893, r2:-41.23173538595784, mse = 1.5244823914254084

Sentiment analysis of top 5 picks:
     Bearish Neutral Bullish Total/Compound
BABA   0.177   0.569   0.523         -0.001
NVDA   0.066   0.800   0.741          0.016
PLTR   0.296   0.478   1.604         -0.095
TSLA   0.152   0.762   0.528         -0.048
GME    0.090   0.801   0.405          0.003



## Data:
Includes US stocks with market cap > 100 Million, and price above $3. It doesn't include penny stocks.\
You can download data from here:\
Source (US stocks):  https://www.nasdaq.com/market-activity/stocks/screener?exchange=nasdaq&letter=0&render=download\


Limitations:
It depends mainly on the defined parameters for current implementation:
It completely ignores the heavily downvoted comments, and there can be a time when
the most mentioned ticker is heavily downvoted, but you can change that in the upvotes variable.


