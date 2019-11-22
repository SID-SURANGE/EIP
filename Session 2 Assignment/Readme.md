
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
  <li> Parameters - 11,290
  <li> Epochs - 16
  <li> Acc - 99.47
</ul>
<h3> Test Accuracy </h3>
<p> [0.021058968016004927, 0.9947] </p>


<h3> Training epochs log </h3>
<p><b>
  Train on 60000 samples, validate on 10000 samples
Epoch 1/16

Epoch 00001: LearningRateScheduler setting learning rate to 0.01.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0412 - acc: 0.9874 - val_loss: 0.0286 - val_acc: 0.9920
Epoch 2/16

Epoch 00002: LearningRateScheduler setting learning rate to 0.0075815011.
60000/60000 [==============================] - 8s 134us/step - loss: 0.0282 - acc: 0.9906 - val_loss: 0.0237 - val_acc: 0.9922
Epoch 3/16

Epoch 00003: LearningRateScheduler setting learning rate to 0.0061050061.
60000/60000 [==============================] - 8s 138us/step - loss: 0.0227 - acc: 0.9930 - val_loss: 0.0243 - val_acc: 0.9933
Epoch 4/16

Epoch 00004: LearningRateScheduler setting learning rate to 0.005109862.
60000/60000 [==============================] - 8s 132us/step - loss: 0.0200 - acc: 0.9937 - val_loss: 0.0247 - val_acc: 0.9920
Epoch 5/16

Epoch 00005: LearningRateScheduler setting learning rate to 0.0043936731.
60000/60000 [==============================] - 8s 136us/step - loss: 0.0178 - acc: 0.9941 - val_loss: 0.0221 - val_acc: 0.9936
Epoch 6/16

Epoch 00006: LearningRateScheduler setting learning rate to 0.0038535645.
60000/60000 [==============================] - 8s 132us/step - loss: 0.0166 - acc: 0.9947 - val_loss: 0.0226 - val_acc: 0.9936
Epoch 7/16

Epoch 00007: LearningRateScheduler setting learning rate to 0.003431709.
60000/60000 [==============================] - 8s 132us/step - loss: 0.0148 - acc: 0.9951 - val_loss: 0.0225 - val_acc: 0.9936
Epoch 8/16

Epoch 00008: LearningRateScheduler setting learning rate to 0.0030931024.
60000/60000 [==============================] - 8s 129us/step - loss: 0.0137 - acc: 0.9953 - val_loss: 0.0202 - val_acc: 0.9941
Epoch 9/16

Epoch 00009: LearningRateScheduler setting learning rate to 0.0028153153.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0149 - acc: 0.9951 - val_loss: 0.0226 - val_acc: 0.9936
Epoch 10/16

Epoch 00010: LearningRateScheduler setting learning rate to 0.0025833118.
60000/60000 [==============================] - 8s 132us/step - loss: 0.0126 - acc: 0.9959 - val_loss: 0.0228 - val_acc: 0.9936
Epoch 11/16

Epoch 00011: LearningRateScheduler setting learning rate to 0.0023866348.
60000/60000 [==============================] - 8s 126us/step - loss: 0.0105 - acc: 0.9967 - val_loss: 0.0239 - val_acc: 0.9931
Epoch 12/16

Epoch 00012: LearningRateScheduler setting learning rate to 0.0022177866.
60000/60000 [==============================] - 8s 138us/step - loss: 0.0117 - acc: 0.9958 - val_loss: 0.0216 - val_acc: 0.9933
Epoch 13/16

Epoch 00013: LearningRateScheduler setting learning rate to 0.002071251.
60000/60000 [==============================] - 8s 133us/step - loss: 0.0114 - acc: 0.9961 - val_loss: 0.0207 - val_acc: 0.9944
Epoch 14/16

Epoch 00014: LearningRateScheduler setting learning rate to 0.0019428793.
60000/60000 [==============================] - 8s 131us/step - loss: 0.0100 - acc: 0.9966 - val_loss: 0.0215 - val_acc: 0.9944
Epoch 15/16

Epoch 00015: LearningRateScheduler setting learning rate to 0.0018294914.
60000/60000 [==============================] - 8s 131us/step - loss: 0.0104 - acc: 0.9966 - val_loss: 0.0207 - val_acc: 0.9940
Epoch 16/16

Epoch 00016: LearningRateScheduler setting learning rate to 0.0017286085.
60000/60000 [==============================] - 8s 130us/step - loss: 0.0098 - acc: 0.9968 - val_loss: 0.0211 - val_acc: 0.9947
<keras.callbacks.History at 0x7fc6e91815f8>
</b>
</p>
<hr>
<p> Siddharth Surange</p>
