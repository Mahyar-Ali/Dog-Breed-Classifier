# Dog-Breed-Classifier
Predicting the Breed of a Dog using Transfer learning in Keras 
-----------------------------------------------------------------------------------

Predicting the breed of a dog is quite a huge task but we can make this task simple using transfer learning.
In this notebook I have used Transfer Learning on pretained models. The models which I selected for this task are 
- XCEPTION
- RESNET152V2

Both models were trained on the imagenet dataset.
I am using Keras in this Notebook. The most important reason is that both of thses models can easily be downloaded
and preprocessed using Keras.

A liitle Insight on the Performance.

- RESNET152V2 
[Note every architecture includes the first GlobalAveragePooling layer]
No Hidden Layer :
Accuracy [Trainig Set : ~99.8% , Validation Set: ~67%]
One Hidden Layer, No Dropout
Accuracy [Trainig Set : ~99.8% , Validation Set: ~63%]
One Hidden Layer, Dropout rate = 0.5
Accuracy [Trainig Set : ~99.0% , Validation Set: ~74%]
One Hidden Layer, Dropout rate = 0.8
Accuracy [Trainig Set : ~97.0% , Validation Set: ~81%]
One Hidden Layer, Dropout rate = 0.9
Accuracy [Trainig Set : ~91.0% , Validation Set: ~82%]
Two Hidden Layers, Dropout rate = 0.9 each</br> I had to train the model for quite a long time[about 700 epochs] 
but the model seemed to be stuck at the same accuracy. Maybe for training about 5000-10,000 epochs, we can see 
better results. But I am not quite sure.
Accuracy [Trainig Set : ~75.0% , Validation Set: ~71%]
Two Hidden Layers, Dropout rate = 0.8 each
Accuracy [Trainig Set : ~79.0% , Validation Set: ~70%]
I did not try to lower the dropout because you can clearly see where the model is headed. Overfitting!

- XCEPTION
No Hidden Layer :
Accuracy [Trainig Set : ~99.8% , Validation Set: ~86%]

Clearly the Xception model was better in this case. The reason is quite obvious, Overfitting! 
ResNet152v2 is very deep model and as we do not have a large dataset, the model would easily overfit to the dataset.
So,model [using transfering learning on] Xception is better by about 6% accuracy on training set.

ResNet152v2 : ~80% accuracy on test set. </br> Xception : ~86% accuracy on test set

----------------------------------------------------------------------------------------
author : m.mahyarali   --- April 18,2020
