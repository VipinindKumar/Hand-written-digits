# Hand-written-digits
Machine learning project in python for training and prediction of the images for hand written digits.

## Digits notebook:
Simple Support Vector Machine Model to predict last image of the sklearn digits dataset, by training the model on rest of the 1796 images of the hand written digits.

## Digits2 notebook:
- Support Vector Machine model
- sklearn digits dataset
- 70% train and 30% for test/dev
- 97% accuracy on the dev set

## HandWrittenDigits notebook:
### optimizer='Adam', loss='mean_squared_error', metrics=['accuracy']
 - **recogModel**
    - 40 epochs, no dropout
    
    set | loss | accuracy
   ------------ | ------------ | -------------
    train | 6.1613e-04 | 0.9962378
    test | 0.0024366 | 0.98595
    
    - 50 epochs (lead to a little overfitting)
    
    set | loss | accuracy
   ------------ | ------------ | -------------
    train | 5.6148e-04 | 0.9968
    test | 0.0026 | 0.9857
    
    - Batch normalization, no dropout, 50 epochs, batch size 50
    
    set | loss | accuracy
   ------------ | ------------ | -------------
    train | 3.3942e-04 | 0.9981
    test | 0.0022056 | 0.9869
    competition | 1001(rank) | 0.98757
    
    - things to try:
      - add regularization
      - keras imageDataGenerator
      - learning rate changer
      - new model
    
    - dropout in dense layer
    
    set | loss | accuracy
   ------------ | ------------ | -------------
    train | 7.4835e-04 | 0.9956
    test | 0.0022165 | 0.9876
    competition | 943(rank) | 0.98885
    
    - ImageDataGenerator for training, 30 epochs, steps per epoch 840
    
    set | loss | accuracy
   ------------ | ------------ | -------------
    train | 0.0030 | 0.9811
    test | 0.0020 | 0.9869
    competition | - | 0.98771
    - steps per epoch 1400
    
    set | loss | accuracy
   ------------ | ------------ | -------------
    train | - | -
    test | 0.00168 | 0.990476
    competition | - | 0.99185
    
    - Reduce learning rate to half after no change in 3 epochs, 50 epochs
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    test | 0.00144 | 0.98976
    competition | - | 0.99128
    
    - things to try:
      - change model
      - change parameters of ImageDataGeneraor
      
    - steps_per_epoch = X_train.shape[0] / 30, min_lr = 0.0, 30 epochs
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    test | 0.001028 | 0.99380
    competition | ⬆265 | 0.99428
    
    - ImageDataGenerator parameters increase
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    test | 0.001473 | 0.99095
    competition | - | 0.99185
    
    - -dropout in desnse, -last change
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    test | 0.00114 | 0.99309
    competition | - | 0.99257
    
    - L2 regularization in layers (lambda=0.01), 30 epochs
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    test | 0.0437 | 0.9321
    
    - regularize conv layers only, 30 epochs
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    test | 0.001658 | 0.99357
    competition | - | 0.99371
    
 - **newModel**
  
    - 30 epochs
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    test | 0.000656 | 0.99570
    competition | 246(⬆215) | 0.99600
    
    - 50 epochs
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    test | 0.0008436 | 0.99520
    competition | ⬆27 | 0.99614
    
    - Increase ImageDataGenerator arguments
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    test | 0.000768 | 0.99548
    competition | - | 0.99571
    
 - **bigModel**
   - using a larger model (maybe needed to be trained for longer)
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    train | 0.0123 | 0.93850
    test | 0.0055 | 0.97240
    
 - **newModel**
  
    - 75 epochs
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    train | 0.000864 | 0.9949
    test | 0.000697 | 0.9960
    competition | ⬆23 | 0.99628
    
    - 100 epochs
    
    \- | loss | accuracy
   ------------ | ------------ | -------------
    train | 0.0008517 | 0.9947
    test | 0.0006300 | 0.9964
    competition | ⬆39 | 0.99657
