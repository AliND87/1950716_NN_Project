# A description of STLF using derived features and recurrent networks
Short-Term-Load-Forecasting (STLF) is a challenging research direction and in last decade has been received significant attention.
 STLF can be applied on different level of consumption levels ranging from house level to distribution level. The lower the level of consumpption the more volatile the trend of consumption will be. This volatility makes prediction difficult.
Machine Learning solutions proved to be a relible predictor even for one-day ahead forecasting and low level loads(house level).
Recurrent NN are able to capture temporal dependencies of a sequential data and are the main networks which are used for STLF.
Prediction of future load becomes even more difficullt when the dataset is small.
To overcome this obstacle enriching dataset with relevant derived features(hand crafted) is useful.

In this paper a new architecture is proposed which has two parallel branch of sequential network.The first branch is fed by the basic features and the second one by derived features.

Basic features:

E(usage in KW ) , T(the time of the day every 30 min) , W(the day of the week ), H(holiday or weekday)

Derived features:

E(usage in KW) , A(Average load of past k timesteps) , D(Standard Deviation of load of past k timesteps) ,A1(Average load of past k day at time t) ,D1(Standard Deviation of load of past k day at time t)

<hr/>

## My Contribution

1-preprocessing step: the data come from PERCON data set should has been  changed  from one minutes reading interval to 30 minutes and also an small bias is added to reading values to avoid unrealistic Loss values(MAPE) 

2- implement the model from scratch using pytorch(as suggested) and also for different experiment cases as well as different networks(LSTM,GRU,RNN,BLSTM,BGRU,BRNN) 

note: in the original code it is implemented in "Keras" 

3-implement training procedure for pytorch using dataloader and training loop

note: in the original code it is implemented in "Keras" which enables the training and evaluation phases only by one line of code: model.train or model.eval 

<hr/>

## Results 
the rseults are reported in the notebook "NN_1950716.ipynb" as well as github repository https://github.com/AliND87/1950716_NN_Project/tree/main/experiments  

<hr/>

## Requirements and "How-To-Run"
Can be found  in second section of notebook "NN_1950716.ipynb"

<hr/>

 
 <figure>
 <center>
 <img src='https://i.postimg.cc/63Snk5K6/overal-results.png' width="250" 
      height="250"/>
 <figcaption>Training loss</figcaption>
 </center>
 </figure>
 
 <figure>
 <center>
 <img src='https://i.postimg.cc/85PyqLnh/2.png' width="600" 
      height="250"/>
 <figcaption>Actual vs Predicted</figcaption></center>
 </figure>

