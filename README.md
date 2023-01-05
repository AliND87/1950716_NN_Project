# A description of STLF using derived features and recurrent networks
Short-Term-Load-Forecasting (STLF) is a difficult research direction and in last decade has benn received significant attention.
 STLF can be adopted in different level of consumption ranging from house level to distribution level. The lower the level of STLF is the more volatile the trend of consumption. This volatility makes prediction problem  very challanging.
Machine Learning solutions proved to be a relible predictor even for one-day ahead forecasting and  low levels(house level).
Recurrent NN are able to capture temporal dependencies of a sequential data and are the main networks which have been used for STLF.
Prediction of future load even more difficullt  when the data set is small.
To overcome this obstacle enriching dataset with relevant derived features is useful.
In this paper a new architecture is proposed which has two parallel branch of sequential network.The first branch is fed by the basic features and the second one by derived features.
Basic features are: E(usage in KW ) , T(the time of the day every 30 min) , W(the day of the week ), H(holiday or weekday)
Derived features: E(usage in KW) , A(Average load of past k timesteps) , D(Standard Deviation of load of past k timesteps) ,A1(Average load of past k day at time t) ,D1(Standard Deviation of load of past k day at time t)

