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
        
![Image alt](https://github.com/maggiemmae/lab_3/blob/master/epoch_categorical_accuracy%20exp.svg)
![Image alt](https://github.com/maggiemmae/lab_3/blob/master/epoch_loss%20exp.svg)
