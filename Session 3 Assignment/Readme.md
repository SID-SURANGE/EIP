<h1> Session 3 Assignment </h1><hr>
<h3> Base Model accuracy </h3> 
<p> Accuracy on test data is: 82.64 </p>
<hr>
<h3> Final Model accuracy </h3> 
<p> Last epoch val Accuracy - 84.19 </p>
<p> Overall highest val Accuracy - 85.29 </p>
<hr>
<h3> Final Model arhitecture </h3>
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
390/390 [==============================] - 57s 147ms/step - loss: 0.7364 - acc: 0.7509 - val_loss: 0.6998 - val_acc: 0.7661<br>
Epoch 2/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.6955 - acc: 0.7643 - val_loss: 0.7000 - val_acc: 0.7646<br>
Epoch 3/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.6620 - acc: 0.7749 - val_loss: 0.6598 - val_acc: 0.7786<br>
Epoch 4/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.6283 - acc: 0.7861 - val_loss: 0.7131 - val_acc: 0.7602<br>
Epoch 5/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.6105 - acc: 0.7933 - val_loss: 0.6360 - val_acc: 0.7849<br>
Epoch 6/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.5919 - acc: 0.7976 - val_loss: 0.6502 - val_acc: 0.7810<br>
Epoch 7/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.5745 - acc: 0.8037 - val_loss: 0.6177 - val_acc: 0.7886<br>
Epoch 8/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.5568 - acc: 0.8101 - val_loss: 0.6364 - val_acc: 0.7863<br>
Epoch 9/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.5436 - acc: 0.8127 - val_loss: 0.6462 - val_acc: 0.7830<br>
Epoch 10/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.5268 - acc: 0.8215 - val_loss: 0.7179 - val_acc: 0.7641<br>
Epoch 11/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.5168 - acc: 0.8221 - val_loss: 0.5986 - val_acc: 0.7980<br>
Epoch 12/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.5072 - acc: 0.8259 - val_loss: 0.5842 - val_acc: 0.8008<br>
Epoch 13/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.4965 - acc: 0.8306 - val_loss: 0.5479 - val_acc: 0.8149<br>
Epoch 14/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.4879 - acc: 0.8329 - val_loss: 0.5472 - val_acc: 0.8175<br>
Epoch 15/50
390/390 [==============================] - 47s 119ms/step - loss: 0.4716 - acc: 0.8385 - val_loss: 0.5224 - val_acc: 0.8216<br>
Epoch 16/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.4648 - acc: 0.8385 - val_loss: 0.5668 - val_acc: 0.8090<br>
Epoch 17/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.4625 - acc: 0.8424 - val_loss: 0.5941 - val_acc: 0.8062<br>
Epoch 18/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.4619 - acc: 0.8420 - val_loss: 0.5123 - val_acc: 0.8255<br>
Epoch 19/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.4385 - acc: 0.8506 - val_loss: 0.5542 - val_acc: 0.8146<br>
Epoch 20/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.4401 - acc: 0.8501 - val_loss: 0.5006 - val_acc: 0.8298<br>
Epoch 21/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.4343 - acc: 0.8534 - val_loss: 0.5106 - val_acc: 0.8273<br>
Epoch 22/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.4253 - acc: 0.8541 - val_loss: 0.5657 - val_acc: 0.8082<br>
Epoch 23/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.4187 - acc: 0.8582 - val_loss: 0.5120 - val_acc: 0.8303<br>
Epoch 24/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.4152 - acc: 0.8564 - val_loss: 0.5041 - val_acc: 0.8275<br>
Epoch 25/50<br>
390/390 [==============================] - 46s 119ms/step - loss: 0.4132 - acc: 0.8577 - val_loss: 0.5482 - val_acc: 0.8218<br>
Epoch 26/50<br>
390/390 [==============================] - 46s 119ms/step - loss: 0.4041 - acc: 0.8619 - val_loss: 0.5864 - val_acc: 0.8074<br>
Epoch 27/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.4041 - acc: 0.8622 - val_loss: 0.4599 - val_acc: 0.8479<br>
Epoch 28/50
390/390 [==============================] - 46s 119ms/step - loss: 0.3992 - acc: 0.8633 - val_loss: 0.5525 - val_acc: 0.8148<br>
Epoch 29/50<br>
390/390 [==============================] - 46s 119ms/step - loss: 0.3957 - acc: 0.8638 - val_loss: 0.4859 - val_acc: 0.8343<br>
Epoch 30/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3919 - acc: 0.8643 - val_loss: 0.4895 - val_acc: 0.8355<br>
Epoch 31/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3858 - acc: 0.8652 - val_loss: 0.5468 - val_acc: 0.8149<br>
Epoch 32/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3766 - acc: 0.8701 - val_loss: 0.4909 - val_acc: 0.8364<br>
Epoch 33/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3812 - acc: 0.8676 - val_loss: 0.5187 - val_acc: 0.8254<br>
Epoch 34/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3717 - acc: 0.8723 - val_loss: 0.4810 - val_acc: 0.8395<br>
Epoch 35/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3708 - acc: 0.8719 - val_loss: 0.5462 - val_acc: 0.8176<br>
Epoch 36/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.3704 - acc: 0.8721 - val_loss: 0.4875 - val_acc: 0.8346<br>
Epoch 37/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3635 - acc: 0.8747 - val_loss: 0.4823 - val_acc: 0.8347<br>
Epoch 38/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.3562 - acc: 0.8767 - val_loss: 0.5590 - val_acc: 0.8133<br>
Epoch 39/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3578 - acc: 0.8762 - val_loss: 0.4879 - val_acc: 0.8394<br>
Epoch 40/50<br>
390/390 [==============================] - 46s 119ms/step - loss: 0.3592 - acc: 0.8743 - val_loss: 0.4677 - val_acc: 0.8420<br>
Epoch 41/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3513 - acc: 0.8775 - val_loss: 0.4663 - val_acc: 0.8407<br>
Epoch 42/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3470 - acc: 0.8795 - val_loss: 0.4583 - val_acc: 0.8498<br>
Epoch 43/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3449 - acc: 0.8804 - val_loss: 0.4568 - val_acc: 0.8481<br>
Epoch 44/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.3432 - acc: 0.8807 - val_loss: 0.4904 - val_acc: 0.8348<br>
Epoch 45/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.3411 - acc: 0.8823 - val_loss: 0.4888 - val_acc: 0.8331<br>
Epoch 46/50<br>
390/390 [==============================] - 47s 119ms/step - loss: 0.3395 - acc: 0.8817 - val_loss: 0.4435 - val_acc: 0.8503<br>
Epoch 47/50<br>
390/390 [==============================] - 46s 119ms/step - loss: 0.3345 - acc: 0.8840 - val_loss: 0.4679 - val_acc: 0.8413<br>
Epoch 48/50<br>
390/390 [==============================] - 46s 119ms/step - loss: 0.3320 - acc: 0.8848 - val_loss: 0.4333 - val_acc: 0.8529<br>
Epoch 49/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3296 - acc: 0.8853 - val_loss: 0.4477 - val_acc: 0.8487<br>
Epoch 50/50<br>
390/390 [==============================] - 47s 120ms/step - loss: 0.3311 - acc: 0.8841 - val_loss: 0.4752 - val_acc: 0.8419<br>
Model took 2344.02 seconds to train
</b></p>
