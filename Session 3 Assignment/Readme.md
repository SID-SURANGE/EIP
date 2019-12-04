<h1> Session 3 Assignment </h1><hr>
<h3> Base Model accuracy </h3> 
<p> Accuracy on test data is: 82.14 </p>
<hr>
<h3> Final Model accuracy </h3> 
<p> Last epoch val Accuracy - 84.65 </p>
<p> Overall highest val Accuracy - 85.58 </p>
<P><b> Total parameters</b> - 65101 </P>
<hr>
<h3> Final Model arhitecture </h3>
'''
model1 = Sequential()
'''
<p>
model1 = Sequential()<br>

<b> #BLOCK 1 </b><br>
model1.add(SeparableConv2D(64, kernel_size=(3, 3), activation='relu', input_shape=(32, 32, 3), padding='same'))<B>  Output - 32/32/64, RF-3 </B><br>
model1.add(BatchNormalization())<br>

model1.add(SeparableConv2D(64, kernel_size=(3, 3), activation='relu')) <b>Output - 30/30/64, RF-5</B><br>
model1.add(BatchNormalization())<br>
model1.add(Dropout(0.1))<br>

model1.add(SeparableConv2D(128, kernel_size=(3, 3), activation='relu', padding='same'))<B> Output - 30/30/128, RF-7</b><br>
model1.add(BatchNormalization())<br>
model1.add(Dropout(0.1))<br>

model1.add(MaxPooling2D(pool_size=(2, 2)))<B>Output- 15/15/128 , RF - 8</B><br> 

<b>#BLOCK 2</b><br>
model1.add(Conv2D(64, 1, 1 , activation='relu')) <B> Output 15/15/64, RF - 8</B><br>
model1.add(BatchNormalization())<br>
model1.add(Dropout(0.1))<br>

model1.add(SeparableConv2D(96, kernel_size=(3, 3), activation='relu',padding='same')) <B>Output - 15/15/96 , RF - 12</B><br>
model1.add(BatchNormalization())<br>
model1.add(Dropout(0.1))<br>

model1.add(SeparableConv2D(128, kernel_size=(3, 3), activation='relu')) <B>Output - 13/13/128 RF - 16</B><br>
model1.add(BatchNormalization())<br>
model1.add(Dropout(0.15))<br>

model1.add(MaxPooling2D(pool_size=(2, 2))) <B>Output - 6/6/128, RF - 18</b><br>

<b>#FINAL BLOCK</b><br>
model1.add(SeparableConv2D(128, kernel_size=(3, 3), activation='relu')) <b> Output - 4/4/128, RF - 26</B><br>
model1.add(BatchNormalization())<br>
model1.add(Dropout(0.15))<br>

model1.add(SeparableConv2D(10, kernel_size=(3, 3), activation='relu')) <B> Output - 2/2/10 , RF - 34 </B><br>
model1.add(BatchNormalization())<br>

model1.add(GlobalAveragePooling2D()) #1/1/10<br>
model1.add(Activation('softmax'))<br>
</p>
<hr>

<h3> Epoch Logs </h3>
<p><b>
Epoch 1/50<br>
390/390 [==============================] - 27s 70ms/step - loss: 1.5205 - acc: 0.4752 - val_loss: 1.1740 - val_acc: 0.5980<br>
Epoch 2/50<br>
390/390 [==============================] - 25s 65ms/step - loss: 1.1183 - acc: 0.6274 - val_loss: 1.0272 - val_acc: 0.6528<br>
Epoch 3/50<br>
390/390 [==============================] - 25s 65ms/step - loss: 0.9540 - acc: 0.6842 - val_loss: 0.9611 - val_acc: 0.6773<br>
Epoch 4/50<br>
390/390 [==============================] - 25s 65ms/step - loss: 0.8522 - acc: 0.7153 - val_loss: 0.9946 - val_acc: 0.6664<br>
Epoch 5/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.7847 - acc: 0.7365 - val_loss: 0.8870 - val_acc: 0.7024<br>
Epoch 6/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.7352 - acc: 0.7519 - val_loss: 0.9546 - val_acc: 0.6794<br>
Epoch 7/50<br>
390/390 [==============================] - 25s 65ms/step - loss: 0.6934 - acc: 0.7665 - val_loss: 0.7419 - val_acc: 0.7511<br>
Epoch 8/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.6638 - acc: 0.7765 - val_loss: 0.8012 - val_acc: 0.7366<br>
Epoch 9/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.6414 - acc: 0.7822 - val_loss: 0.7260 - val_acc: 0.7519<br>
Epoch 10/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.6151 - acc: 0.7893 - val_loss: 0.6269 - val_acc: 0.7895<br>
Epoch 11/50<br>
390/390 [==============================] - 25s 65ms/step - loss: 0.5974 - acc: 0.7973 - val_loss: 0.5972 - val_acc: 0.8028<br>
Epoch 12/50<br>
390/390 [==============================] - 25s 65ms/step - loss: 0.5784 - acc: 0.8030 - val_loss: 0.7209 - val_acc: 0.7593<br>
Epoch 13/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.5640 - acc: 0.8084 - val_loss: 0.6242 - val_acc: 0.7900<br>
Epoch 14/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.5457 - acc: 0.8126 - val_loss: 0.6102 - val_acc: 0.7931<br>
Epoch 15/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.5329 - acc: 0.8180 - val_loss: 0.5976 - val_acc: 0.7991<br>
Epoch 16/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.5196 - acc: 0.8247 - val_loss: 0.6031 - val_acc: 0.7948<br>
Epoch 17/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.5138 - acc: 0.8247 - val_loss: 0.5728 - val_acc: 0.8062<br>
Epoch 18/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.5026 - acc: 0.8252 - val_loss: 0.5403 - val_acc: 0.8194<br>
Epoch 19/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4931 - acc: 0.8308 - val_loss: 0.5457 - val_acc: 0.8142<br>
Epoch 20/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4805 - acc: 0.8355 - val_loss: 0.5318 - val_acc: 0.8207<br>
Epoch 21/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4742 - acc: 0.8371 - val_loss: 0.5312 - val_acc: 0.8250<br>
Epoch 22/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4673 - acc: 0.8392 - val_loss: 0.5511 - val_acc: 0.8186<br>
Epoch 23/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4545 - acc: 0.8440 - val_loss: 0.5348 - val_acc: 0.8185<br>
Epoch 24/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4532 - acc: 0.8424 - val_loss: 0.5562 - val_acc: 0.8193<br>
Epoch 25/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4465 - acc: 0.8464 - val_loss: 0.5381 - val_acc: 0.8201<br>
Epoch 26/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4418 - acc: 0.8483 - val_loss: 0.4953 - val_acc: 0.8337<br>
Epoch 27/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4372 - acc: 0.8480 - val_loss: 0.4984 - val_acc: 0.8290<br>
Epoch 28/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4310 - acc: 0.8517 - val_loss: 0.5302 - val_acc: 0.8225<br>
Epoch 29/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4248 - acc: 0.8540 - val_loss: 0.5299 - val_acc: 0.8251<br>
Epoch 30/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.4183 - acc: 0.8545 - val_loss: 0.5537 - val_acc: 0.8152<br>
Epoch 31/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4187 - acc: 0.8562 - val_loss: 0.4972 - val_acc: 0.8336<br>
Epoch 32/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4081 - acc: 0.8591 - val_loss: 0.5163 - val_acc: 0.8286<br>
Epoch 33/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.4024 - acc: 0.8596 - val_loss: 0.5041 - val_acc: 0.8333<br>
Epoch 34/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.3995 - acc: 0.8620 - val_loss: 0.4991 - val_acc: 0.8357<br>
Epoch 35/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.3982 - acc: 0.8637 - val_loss: 0.4960 - val_acc: 0.8337<br>
Epoch 36/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.3959 - acc: 0.8635 - val_loss: 0.5351 - val_acc: 0.8267<br>
Epoch 37/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.3839 - acc: 0.8674 - val_loss: 0.4705 - val_acc: 0.8459<br>
Epoch 38/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.3875 - acc: 0.8651 - val_loss: 0.4887 - val_acc: 0.8400<br>
Epoch 39/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.3866 - acc: 0.8665 - val_loss: 0.5375 - val_acc: 0.8222<br>
Epoch 40/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.3780 - acc: 0.8712 - val_loss: 0.5062 - val_acc: 0.8355<br>
Epoch 41/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.3774 - acc: 0.8693 - val_loss: 0.5055 - val_acc: 0.8367<br>
Epoch 42/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.3755 - acc: 0.8700 - val_loss: 0.5736 - val_acc: 0.8126<br>
Epoch 43/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.3738 - acc: 0.8698 - val_loss: 0.4727 - val_acc: 0.8447<br>
Epoch 44/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.3679 - acc: 0.8714 - val_loss: 0.5051 - val_acc: 0.8337<br>
Epoch 45/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.3649 - acc: 0.8718 - val_loss: 0.5290 - val_acc: 0.8276<br>
Epoch 46/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.3675 - acc: 0.8726 - val_loss: 0.4962 - val_acc: 0.8352<br>
Epoch 47/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.3585 - acc: 0.8752 - val_loss: 0.5442 - val_acc: 0.8267<br>
Epoch 48/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.3546 - acc: 0.8777 - val_loss: 0.4980 - val_acc: 0.8402<br>
Epoch 49/50<br>
390/390 [==============================] - 25s 64ms/step - loss: 0.3579 - acc: 0.8759 - val_loss: 0.4387 - val_acc: 0.8558<br>
Epoch 50/50<br>
390/390 [==============================] - 25s 63ms/step - loss: 0.3490 - acc: 0.8780 - val_loss: 0.4638 - val_acc: 0.8465<br>
Model took 1249.96 seconds to train
 </b></p>
