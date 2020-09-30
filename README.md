# lab_3
1. Step_Decay

       def scheduler(epoch, lr):
          if epoch==40 or epoch==70:
            return lr*0.1
          else:
            return lr
        
![Image alt](https://github.com/maggiemmae/lab_3/blob/master/epoch_categorical_accuracy%20step.svg)
![Image alt](https://github.com/maggiemmae/lab_3/blob/master/epoch_loss%20step.svg)

2. Exponentional Decay

        def scheduler(epoch, lr):
          if epoch < 10:
            return lr
          else:
            return lr * tf.math.exp(-0.1)
         
![Image alt](https://github.com/maggiemmae/lab_3/blob/master/epoch_categorical_accuracy%20exponential.svg)
![Image alt](https://github.com/maggiemmae/lab_3/blob/master/epoch_loss%20exponential.svg)

3.Warm-Up

     def scheduler(epoch, lr):
       initial_lrate = 0.00001
       a = 0
       b = 0.00001
       k = 0.1
       if epoch <= 10:
           return ((b - a) / 10) * (epoch - 1)
       else:
           return initial_lrate * tf.math.exp(-0.1) 
           
![Image alt](https://github.com/maggiemmae/lab_3/blob/master/epoch_categorical_accuracy%20warm.svg)
![Image alt](https://github.com/maggiemmae/lab_3/blob/master/epoch_loss%20warm.svg)

