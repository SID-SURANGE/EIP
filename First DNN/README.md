 <h2><b>Important terms in Computer Vision -</b></h2><br>                                    
<ol>
  <li><b> Convolution </b></li>
      Operation wherein we use feature extractors(kernels) to extract different set of features by convolving kernels over original input image 
  <li><b> Filters/Kernels </b></li>
      These are the Feature extractors which extract edges, patterns, gradients out from image and creates feature map when convolved.
  <li><b> Epochs </b></li>
      No of iterations over the whole dataset to perform model training.
  <li><b> 1x1 Convolution </b></li>
      Powerful convolutions kernel size to extract the featues required and at the sametime reduce the computation cost.
  <li><b> 3x3 Convolution </b></li>
      Basic kernel size for any CNN and it can imitate any high order kernel(9*9,13*13) by applying some extra 3*3 convolutions
      with minimum parameters to train.
  <li><b> Feature Maps </b></li>
      Output of filter operations applied over an input image or image in intermediate layers in CNN. It contains all features extracted.
  <li><b> Activation Function </b></li>
      Function that adds non-linearity to model so that it can learn complex tasks.
  <li><b> Receptive Field </b></li>
      RF is the region of image which produces a particular channel/pixel. It can be Global or Local.<br>
      1) GlobalRF links to region of initial input image.<br>
      2) LocalRF is region/pixels from the previous layer which generates current pixel.
</ol>

<h3> Final Test Score</h3>
 <p> Accuracy - 99.16%</p>
   
Notes By - Siddharth Surange
