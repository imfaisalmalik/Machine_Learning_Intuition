# Week 3 Summary


## 1. Binary Classification Problem
- Two possible classess/categories
- Output (y) can be one of two values 
- Only 2 possible output values, e.g., yes/no, 1/0, true/false, positive/negative, presence/absence
- Here `positive` and `negative` doesn't mean `good` or `bad` instead `poitive class` means the `presence` and `neagative class` means the `absence` of something.

## 2. Decision Boundry
- Dividing line where we are neautral. 

## 3. Why Linear Regression is not a good algorithm for classification?
- Adding a single data point (say at right) can change the decision boundry, i.e., our conclusion about how to classify data, e.g., `malignant tumor` vs `benign tumor`. 
- The problem is that, decision boundry isn't generaized and keeps on changing as you add more examples.Thus changing decision boundry, can end up with a worse function for classification problem.
- Our goal is to come up with a genralized decision boundry that doesn't `change significantly` by adding new examples to dataset.
- Sometimes, `Linear Regression` can work for classification, but often doesn't work very well.

## 4. Sigmoid Function
- Also known as logistic function.

- The formula for a sigmoid function is as follows -  

$$ g(z) = \frac{1}{1+e^{-z}} \tag{1}$$

- In the case of logistic regression, z (the input to the sigmoid function), is the output of a linear regression model. 
    - In the case of a single example, $z$ is scalar.
    - In the case of multiple examples, $z$ may be a vector consisting of $m$ values, one for each example.
    - `Sigmoid function` >> a **Non-linear component** used to **add Non-linearity** in the output (z) of `linear regression` and makes it a `logistic regression` and capable of drawing non-linear decision boundry.

## 5. Logistic Regression
- A classification algorithm, outputs probability of y = 1
- Works over `Signmoid function`
- Build in 2 steps:
    > 1. Calculate z(x), i.e., f(x) for linear regression 
    > 2. Calculate g(z) = sigmoid(z)

## 6. Why `squared error cost` function isn't suitable for `logistic regression`?
- In case of `linear regression` the `squared error cost` function generates a **convex curve**, i.e., a curve having same (single) local and global minimum.
- In case of `logistic regression` the `squared error cost` function generates a **Non-convex curve**, i.e., a curve having multiple local minima, so we have to find multiple local minima to reach global minima.
- That's why `squared error cost` function not suitable for logistic regression. Thus, we used another loss function, given as:

    $$loss(f_{\mathbf{w},b}(\mathbf{x}^{(i)}), y^{(i)}) = (-y^{(i)} \log\left(f_{\mathbf{w},b}\left( \mathbf{x}^{(i)} \right) \right) - \left( 1 - y^{(i)}\right) \log \left( 1 - f_{\mathbf{w},b}\left( \mathbf{x}^{(i)} \right) \right)$$

- The above loss function is also known as: `Logistic Loss` function.
- The curve of `logistic loss function` is well suited to gradient descent! It does not have plateaus, local minima, or discontinuities. Note, it is not necessary to always have a  `bowl shape` curve as in the case of squared error.

## 7. Loss vs Cost
- Loss is a measure of the difference of a single example to its target value.
- Cost is a measure of all losses over the training set

## 8. Regularization
- used to reduce overfitting

## 9. Overfitting vs Underfitting
- `Overfitting` High Varience means high variation in model fitting curve.
- `Underfitting` High Bias means model prediction is biased towards some class.

## 10. Three Things to Consider About Every Machine Learning Algorithm
- Model Function / Equation `f(x)`
- Cost Function `J(w,b)`
- How to minimize cost using Gradient Descent or some other algorithm? `min J(w,b)`