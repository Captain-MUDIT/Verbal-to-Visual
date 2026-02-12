# COURSE2-WEEK2
## MINI BATCH
If the dataset is very large like 5 million data then even using vectorization the model may become slow , so we divide the dataset into mini batches of dataset and rum the model seperatly on each mini batch
![alt text](image-13.png)
![alt text](image-14.png)
one epoch is one pass through a training set for one batch the one epoch generates one gradient descent and for 5000 mini batches it generates 5000 gradient descent.
![alt text](image-15.png)
as we can see if we take the whole batch as one then the iteration will take long time.

if we take mini batch as 1 input then it will loose the speeding gained by vectorization .

So the best option is to mske mini batchs so that we have the advantage of the vectorization and the iterations are also fast
![alt text](image-16.png)
## EXPONENTIALLY WEIGHTED AVERAGE
An exponentially weighted average (EWA) is a type of moving average that gives more weight to recent data points while gradually reducing the weight of older points. It's useful in time series analysis for smoothing data and capturing trends.
Here $\beta$ is constant.
![alt text](image-17.png)
![alt text](image-18.png)
![alt text](image-19.png)
Bias correction is used in exponentially weighted averages to address the fact that, especially at the beginning of the time series, the average may be biased towards the initial values. This bias occurs because the exponentially weighted average starts with an initial value (0).
![alt text](image-20.png)
## Gradient Descent With Momentum
As we can see in the image the way of gradient descent reaaching the minima can be made faster by toning dwon the way like we see in EWS. This helps the learning to be fast. We clearly use EWS in it
![alt text](image-21.png)
![alt text](image-22.png)
## RMSProp
It is one of the way to optimize our model.As we can see in the example that we want to reduce our travel in veritical direction and increse it in horizontal direction.
![alt text](image-23.png)
## Adam Optimization Algorithm
When we merge exponenetially weightes sum and RMSprop in one we get Adam optimization .It is seen to work impressively on many models
![alt text](image-24.png)
![alt text](image-25.png)
## Learning Rate Decay
When we have large learning rate , initially the learning and the movment towards minima is fast but as it reaches the minima it starts to lingar around and does not actually reaches it where else in less learning rate it does not lingar , so we can eventually decrease the learning rate.
![alt text](image-26.png)
![alt text](image-27.png)
![alt text](image-28.png)