# Implementing-SGD-claasifier-from-scratch-without-sckitlearn

In this we are implementing the gradient descent for every step of our algorithm. since its for learning purpose we are using just few hundred datapoints.  
but actual scenario will be around 2million or more datapoints to calculate. In such situation , we use algorithm called the batch gradient descent(we are not entering in this part now ).

The implementation of the regular/classic gradient descent method consists of initially evaluating both the function and its gradient, starting from a configuration chosen randomly in the space of dimensions.

From here, we try to move in the direction indicated by the gradient. This establishes a direction of descent in which the function tends to a minimum and examines whether the function actually takes on a value lower than that calculated in the previous configuration. If so, the procedure continues iteratively, recalculating the new gradient. This can be totally different from the previous one. After this, it starts again in search of a new minimum.

This iterative procedure requires that, at each step, the entire system status is updated. This means that all the parameters of the system must be recalculated. From a computational point of view, this equates to an extremely expensive operating cost and greatly slows down the estimation procedure. With respect to the standard gradient descent method, in which the weights are updated after calculating the gradient for the entire dataset, in the stochastic method, the system parameters are updated after a certain number of examples. These are chosen randomly in order to speed up the process and to try and avoid any local minimum situations.

Consider a dataset that contains n observations of a phenomenon. Here, let f be an objective function that we want to minimize with respect to a series of parameters x. Here, we can write the following equation:

![Screen Shot 2022-01-01 at 12 31 59 AM](https://user-images.githubusercontent.com/73736016/147836396-83849119-0cf0-4f59-9197-e94c732703b6.png)

From the analysis of the previous equation, we can deduce that the evaluation of the objective function f requires n evaluations of the function f, one for each value contained in the dataset.

In the classic gradient descent method, at each step, the function gradient is calculated in correspondence with all the values of the dataset through the following equation:
![Screen Shot 2022-01-01 at 12 33 23 AM](https://user-images.githubusercontent.com/73736016/147836425-173f1f3f-fce2-499c-bc02-18d4a36c6a57.png)

In some cases, the evaluation of the sum present in the previous equation can be particularly expensive, such as when the dataset is particularly large and there is no elementary expression for the objective function. The stochastic descent of the gradient solves this problem by introducing an approximation of the gradient function. At each step, instead of the sum of the gradients being evaluated in correspondence to the data contained in the dataset, the evaluation of the gradient is used only in a random subset of the dataset.







