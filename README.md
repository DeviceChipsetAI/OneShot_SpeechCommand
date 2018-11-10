## OneShot_SpeechCommand
# Background
Speech Command is a basic function for almost all smart devices. with speech command, people could ask device to do something. 

the tradition approach is to train a classfication model with specified command. while different device from different company need differnt command, that means training is inavoidable. 

to fix that issue, we try to introduce one shot learning for speech command. 

We expect one shot speech command will be trained with big dataset. In field, the model will make different between command which is not in the training dataset.  

Till now, we try two algorithm

1, build an one shot model with CNN. unfortunately, it doesn't do well on test set

2, build an one shot model with GRU, it achieves like 65% accuracy on test set, it may not be good enough. while it may be the right direction. 


# practice



Before you try the model mentioned, you have to make sure
1, Python3/Jupyter installed correctly, it verfied on Ubuntu, Windows7 and Mac. 

2, Tensorflow. it was tested with the latest Tensorflor 1.11. It should be run on early version. But it is on your own risk. 

Training Data set
1, the Dataset is coming from Google Speech Command. you can download it from https://storage.cloud.google.com/download.tensorflow.org/data/speech_commands_v0.02.tar.gz. 
   It is behind great wall, you have to figure out how to download it. 
   
   I put a copy in Baidu. you can access it by  https://pan.baidu.com/s/1869OTBiS9HgSpCeZNnKJaA. the access code is izy3. 
   I cannot promise it will always works. try it by yourself. 

2, put the dataset on your local disk and set the directory in notebook before you run the model. 


# Need more helps
Still it is no clear that one shot is good enough for speech command in field. 
We need help in the following topics

1, audio preprocessing. the current model is based on MFCC. We are not audio expert. We expect helps on what is the right features set for speech command. 

2, one key for one shot approach is how to combine two features map from two commands. right now it is using ABS to combine two feature map. definitely it is not the right way. We need help on a better algorthm. 

3, Loss function. 

4, Accuracy on Test set. 


