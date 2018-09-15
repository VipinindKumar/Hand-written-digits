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
