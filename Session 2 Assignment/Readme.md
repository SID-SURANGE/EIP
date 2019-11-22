
<h1> Session 2 Assignment
<hr>
<h3> Strategy taken to reach final accuracy-</h3>
<p> Some points which were considered to build model <br>
  <ul>
    <li> Used different combinations of <b>Conv layers and different kernels</b> to extract features. At some point after many combinations the test and train accuracy difference kept on increasing.</li>
    <li> Then I applied Batch norm and Dropout layers to maintain the test accuracy as close possible to train accuracy</li>
    <li> Above two steps also didn't resulted in good accuracy, further which I tried</li>
    <ol>
      <li> Changing initial learning rate for scheduler </li>
      <li> Trying different Epochs numbers </li>
      <li> Removing some dropout layers or changing drop percentage </li>
      <li> Trying different batch sizes (don't know how this could help model</li>
      <li> Changing kernels count and using different ways to arrange layers </li>
    </ol>
</ul></p>

<h3> Final parameter count and epochs </h3>
<ul>
  <li> Parameters - 14,538
  <li> Epochs - 19
  <li> Acc - 99.44
</ul>
<h3> Test Accuracy </h3>
<p> [0.021058968016004927, 0.9947] </p>


<h3> Training epochs log </h3>
<p><b>
Train on 60000 samples, validate on 10000 samples
Epoch 1/19

Epoch 00001: LearningRateScheduler setting learning rate to 0.01.
60000/60000 [==============================] - 10s 160us/step - loss: 0.0391 - acc: 0.9876 - val_loss: 0.0272 - val_acc: 0.9905
Epoch 2/19

Epoch 00002: LearningRateScheduler setting learning rate to 0.0075815011.
60000/60000 [==============================] - 9s 153us/step - loss: 0.0344 - acc: 0.9893 - val_loss: 0.0367 - val_acc: 0.9889
Epoch 3/19

Epoch 00003: LearningRateScheduler setting learning rate to 0.0061050061.
60000/60000 [==============================] - 9s 153us/step - loss: 0.0305 - acc: 0.9906 - val_loss: 0.0251 - val_acc: 0.9927
Epoch 4/19

Epoch 00004: LearningRateScheduler setting learning rate to 0.005109862.
60000/60000 [==============================] - 10s 160us/step - loss: 0.0297 - acc: 0.9906 - val_loss: 0.0268 - val_acc: 0.9916
Epoch 5/19

Epoch 00005: LearningRateScheduler setting learning rate to 0.0043936731.
60000/60000 [==============================] - 9s 157us/step - loss: 0.0270 - acc: 0.9913 - val_loss: 0.0237 - val_acc: 0.9928
Epoch 6/19

Epoch 00006: LearningRateScheduler setting learning rate to 0.0038535645.
60000/60000 [==============================] - 9s 155us/step - loss: 0.0281 - acc: 0.9909 - val_loss: 0.0226 - val_acc: 0.9932
Epoch 7/19

Epoch 00007: LearningRateScheduler setting learning rate to 0.003431709.
60000/60000 [==============================] - 9s 150us/step - loss: 0.0243 - acc: 0.9923 - val_loss: 0.0216 - val_acc: 0.9943
Epoch 8/19

Epoch 00008: LearningRateScheduler setting learning rate to 0.0030931024.
60000/60000 [==============================] - 9s 157us/step - loss: 0.0241 - acc: 0.9924 - val_loss: 0.0201 - val_acc: 0.9934
Epoch 9/19

Epoch 00009: LearningRateScheduler setting learning rate to 0.0028153153.
60000/60000 [==============================] - 9s 149us/step - loss: 0.0224 - acc: 0.9928 - val_loss: 0.0243 - val_acc: 0.9933
Epoch 10/19

Epoch 00010: LearningRateScheduler setting learning rate to 0.0025833118.
60000/60000 [==============================] - 9s 152us/step - loss: 0.0228 - acc: 0.9928 - val_loss: 0.0220 - val_acc: 0.9939
Epoch 11/19

Epoch 00011: LearningRateScheduler setting learning rate to 0.0023866348.
60000/60000 [==============================] - 9s 149us/step - loss: 0.0226 - acc: 0.9925 - val_loss: 0.0235 - val_acc: 0.9933
Epoch 12/19

Epoch 00012: LearningRateScheduler setting learning rate to 0.0022177866.
60000/60000 [==============================] - 9s 151us/step - loss: 0.0213 - acc: 0.9928 - val_loss: 0.0185 - val_acc: 0.9943
Epoch 13/19

Epoch 00013: LearningRateScheduler setting learning rate to 0.002071251.
60000/60000 [==============================] - 9s 149us/step - loss: 0.0209 - acc: 0.9931 - val_loss: 0.0190 - val_acc: 0.9942
Epoch 14/19

Epoch 00014: LearningRateScheduler setting learning rate to 0.0019428793.
60000/60000 [==============================] - 9s 153us/step - loss: 0.0214 - acc: 0.9933 - val_loss: 0.0199 - val_acc: 0.9943
Epoch 15/19

Epoch 00015: LearningRateScheduler setting learning rate to 0.0018294914.
60000/60000 [==============================] - 9s 154us/step - loss: 0.0201 - acc: 0.9933 - val_loss: 0.0217 - val_acc: 0.9936
Epoch 16/19

Epoch 00016: LearningRateScheduler setting learning rate to 0.0017286085.
60000/60000 [==============================] - 9s 156us/step - loss: 0.0199 - acc: 0.9935 - val_loss: 0.0188 - val_acc: 0.9949
Epoch 17/19

Epoch 00017: LearningRateScheduler setting learning rate to 0.00163827.
60000/60000 [==============================] - 9s 146us/step - loss: 0.0190 - acc: 0.9940 - val_loss: 0.0175 - val_acc: 0.9953
Epoch 18/19

Epoch 00018: LearningRateScheduler setting learning rate to 0.0015569049.
60000/60000 [==============================] - 9s 152us/step - loss: 0.0182 - acc: 0.9941 - val_loss: 0.0183 - val_acc: 0.9946
Epoch 19/19

Epoch 00019: LearningRateScheduler setting learning rate to 0.0014832394.
60000/60000 [==============================] - 9s 149us/step - loss: 0.0188 - acc: 0.9939 - val_loss: 0.0201 - val_acc: 0.9944
<keras.callbacks.History at 0x7fc6c6f5f518>
</b>
</p>
<hr>
<p> Siddharth Surange</p>
