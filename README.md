# NinjaTraderIndicator
This repo contains the indicator that I have developed for my organization ML Trades. These indicator do different type of calculation for data capturing. 
#APMasterIndicator 
Upto v39 of this indicator is capturing data for training AI. AP5,AP7,AP14, and AP21 are slave indicator where APMaster is doing the master job. Client indicator do calculation on Renko Chart 5,7,14, and 21 respectively. After calculation slave indicator store the data on database bar by bar on real time. Another hand ,APMaster will get this data in realtime from the database and perform some statistical calulation and write data to CSV file for AI Training. This data contains 106 columns and superviosed learning models are trained on data for prediction.

APMasterv40,41,42 are updates of APMaster that is being use for prediction purpose. Instead of store the data to csv these version of master data send the data item to AI server using Web Request. AI server return response using Web Request in realtime. And this predicted response is used for trading purpose.

#AI Server is python script that is using Flask for webrequest acceptance and prediction response return job to Ninja Trader Script. RandomForest and LightGBM Models are used for Trade Entery Point prediction. While RESNET101 is used for trade type prediction.
