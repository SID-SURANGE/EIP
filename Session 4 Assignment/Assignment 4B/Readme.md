
<h2> Session 4B assignment </h2><hr>

<h4> Model Accuracy </h4>

```
Test accuracy 50th Epoch - 89.38(Highest)
Augumentation - Cutout
```

<h4> Gradcam Implementation </h4>
<img src="Image1- Gradcam.png"
     alt="Markdown Monster icon"
     style="float: center; margin-right: 10px;"
     height=250
     width=700/>

<img src="Image2-Gradcam.png"
     alt="Markdown Monster icon"
     style="float: center; margin-right: 10px;"
     height=250
     width=700/>
     
<img src="Image3-Gradcam.png"
     alt="Markdown Monster icon"
     style="float: center; margin-right: 10px;"
     height=250
     width=700/>
     
<H4> Epoch Log </h4>

```
Using real-time data augmentation.
Epoch 1/50
782/782 [==============================] - 45s 57ms/step - loss: 1.7248 - acc: 0.4285 - val_loss: 1.5236 - val_acc: 0.5023
Epoch 2/50
782/782 [==============================] - 40s 51ms/step - loss: 1.3275 - acc: 0.5768 - val_loss: 1.3187 - val_acc: 0.5883
Epoch 3/50
782/782 [==============================] - 40s 51ms/step - loss: 1.1644 - acc: 0.6401 - val_loss: 1.6009 - val_acc: 0.5337
Epoch 4/50
782/782 [==============================] - 41s 52ms/step - loss: 1.0482 - acc: 0.6835 - val_loss: 1.1834 - val_acc: 0.6551
Epoch 5/50
782/782 [==============================] - 40s 51ms/step - loss: 0.9792 - acc: 0.7086 - val_loss: 1.2986 - val_acc: 0.6350
Epoch 6/50
782/782 [==============================] - 40s 51ms/step - loss: 0.9277 - acc: 0.7287 - val_loss: 1.0614 - val_acc: 0.6901
Epoch 7/50
782/782 [==============================] - 40s 51ms/step - loss: 0.8849 - acc: 0.7436 - val_loss: 0.9007 - val_acc: 0.7391
Epoch 8/50
782/782 [==============================] - 40s 51ms/step - loss: 0.8468 - acc: 0.7595 - val_loss: 1.0048 - val_acc: 0.7316
Epoch 9/50
782/782 [==============================] - 40s 51ms/step - loss: 0.8180 - acc: 0.7707 - val_loss: 1.0334 - val_acc: 0.7212
Epoch 10/50
782/782 [==============================] - 40s 51ms/step - loss: 0.7892 - acc: 0.7807 - val_loss: 0.7951 - val_acc: 0.7870
Epoch 11/50
782/782 [==============================] - 40s 52ms/step - loss: 0.7670 - acc: 0.7890 - val_loss: 0.8441 - val_acc: 0.7666
Epoch 12/50
782/782 [==============================] - 40s 51ms/step - loss: 0.7480 - acc: 0.7968 - val_loss: 0.7609 - val_acc: 0.7995
Epoch 13/50
782/782 [==============================] - 40s 51ms/step - loss: 0.7378 - acc: 0.7988 - val_loss: 0.9869 - val_acc: 0.7235
Epoch 14/50
782/782 [==============================] - 40s 52ms/step - loss: 0.7200 - acc: 0.8065 - val_loss: 0.8124 - val_acc: 0.7852
Epoch 15/50
782/782 [==============================] - 40s 52ms/step - loss: 0.7023 - acc: 0.8128 - val_loss: 0.8134 - val_acc: 0.7908
Epoch 16/50
782/782 [==============================] - 40s 52ms/step - loss: 0.6951 - acc: 0.8182 - val_loss: 0.7708 - val_acc: 0.7967
Epoch 17/50
782/782 [==============================] - 40s 51ms/step - loss: 0.6843 - acc: 0.8188 - val_loss: 0.7239 - val_acc: 0.8097
Epoch 18/50
782/782 [==============================] - 40s 51ms/step - loss: 0.6733 - acc: 0.8229 - val_loss: 0.8294 - val_acc: 0.7797
Epoch 19/50
782/782 [==============================] - 40s 51ms/step - loss: 0.6629 - acc: 0.8299 - val_loss: 0.7406 - val_acc: 0.8043
Epoch 20/50
782/782 [==============================] - 40s 51ms/step - loss: 0.6542 - acc: 0.8327 - val_loss: 0.8684 - val_acc: 0.7843
Epoch 21/50
782/782 [==============================] - 42s 54ms/step - loss: 0.6453 - acc: 0.8364 - val_loss: 0.7634 - val_acc: 0.8056
Epoch 22/50
782/782 [==============================] - 41s 52ms/step - loss: 0.6431 - acc: 0.8361 - val_loss: 0.8193 - val_acc: 0.7933
Epoch 23/50
782/782 [==============================] - 41s 52ms/step - loss: 0.5518 - acc: 0.8658 - val_loss: 0.6123 - val_acc: 0.8516
Epoch 24/50
782/782 [==============================] - 40s 52ms/step - loss: 0.5281 - acc: 0.8741 - val_loss: 0.6099 - val_acc: 0.8561
Epoch 25/50
782/782 [==============================] - 40s 52ms/step - loss: 0.5146 - acc: 0.8764 - val_loss: 0.5738 - val_acc: 0.8636
Epoch 26/50
782/782 [==============================] - 41s 52ms/step - loss: 0.5086 - acc: 0.8781 - val_loss: 0.5755 - val_acc: 0.8591
Epoch 27/50
782/782 [==============================] - 41s 52ms/step - loss: 0.4936 - acc: 0.8827 - val_loss: 0.5927 - val_acc: 0.8561
Epoch 28/50
782/782 [==============================] - 41s 52ms/step - loss: 0.4885 - acc: 0.8829 - val_loss: 0.5416 - val_acc: 0.8731
Epoch 29/50
782/782 [==============================] - 40s 52ms/step - loss: 0.4821 - acc: 0.8840 - val_loss: 0.5571 - val_acc: 0.8669
Epoch 30/50
782/782 [==============================] - 41s 52ms/step - loss: 0.4727 - acc: 0.8869 - val_loss: 0.5737 - val_acc: 0.8647
Epoch 31/50
782/782 [==============================] - 41s 52ms/step - loss: 0.4672 - acc: 0.8868 - val_loss: 0.5343 - val_acc: 0.8679
Epoch 32/50
782/782 [==============================] - 40s 51ms/step - loss: 0.4584 - acc: 0.8911 - val_loss: 0.5494 - val_acc: 0.8668
Epoch 33/50
782/782 [==============================] - 40s 52ms/step - loss: 0.4516 - acc: 0.8924 - val_loss: 0.5697 - val_acc: 0.8640
Epoch 34/50
782/782 [==============================] - 40s 52ms/step - loss: 0.4538 - acc: 0.8901 - val_loss: 0.5795 - val_acc: 0.8633
Epoch 35/50
782/782 [==============================] - 40s 51ms/step - loss: 0.4419 - acc: 0.8944 - val_loss: 0.5210 - val_acc: 0.8731
Epoch 36/50
782/782 [==============================] - 41s 52ms/step - loss: 0.4386 - acc: 0.8955 - val_loss: 0.4955 - val_acc: 0.8817
Epoch 37/50
782/782 [==============================] - 41s 52ms/step - loss: 0.4358 - acc: 0.8957 - val_loss: 0.5390 - val_acc: 0.8687
Epoch 38/50
782/782 [==============================] - 41s 53ms/step - loss: 0.4356 - acc: 0.8958 - val_loss: 0.5198 - val_acc: 0.8704
Epoch 39/50
782/782 [==============================] - 41s 52ms/step - loss: 0.4238 - acc: 0.8991 - val_loss: 0.5593 - val_acc: 0.8658
Epoch 40/50
782/782 [==============================] - 41s 52ms/step - loss: 0.4207 - acc: 0.9000 - val_loss: 0.5408 - val_acc: 0.8718
Epoch 41/50
782/782 [==============================] - 41s 52ms/step - loss: 0.4188 - acc: 0.9007 - val_loss: 0.5550 - val_acc: 0.8662
Epoch 42/50
782/782 [==============================] - 41s 52ms/step - loss: 0.3863 - acc: 0.9110 - val_loss: 0.4630 - val_acc: 0.8910
Epoch 43/50
782/782 [==============================] - 41s 52ms/step - loss: 0.3747 - acc: 0.9145 - val_loss: 0.4933 - val_acc: 0.8829
Epoch 44/50
782/782 [==============================] - 42s 53ms/step - loss: 0.3721 - acc: 0.9160 - val_loss: 0.4658 - val_acc: 0.8912
Epoch 45/50
782/782 [==============================] - 41s 53ms/step - loss: 0.3621 - acc: 0.9183 - val_loss: 0.4857 - val_acc: 0.8874
Epoch 46/50
782/782 [==============================] - 41s 53ms/step - loss: 0.3622 - acc: 0.9178 - val_loss: 0.5248 - val_acc: 0.8762
Epoch 47/50
782/782 [==============================] - 42s 53ms/step - loss: 0.3561 - acc: 0.9195 - val_loss: 0.4842 - val_acc: 0.8865
Epoch 48/50
782/782 [==============================] - 40s 52ms/step - loss: 0.3476 - acc: 0.9234 - val_loss: 0.4631 - val_acc: 0.8923
Epoch 49/50
782/782 [==============================] - 45s 57ms/step - loss: 0.3403 - acc: 0.9259 - val_loss: 0.4654 - val_acc: 0.8926
Epoch 50/50
782/782 [==============================] - 43s 55ms/step - loss: 0.3398 - acc: 0.9250 - val_loss: 0.4576 - val_acc: 0.8938
```

<h4> Siddharth Surange </h4>
