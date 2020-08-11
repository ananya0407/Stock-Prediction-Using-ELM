# Stock-Prediction-Using-ELM-And-OSELM
ELM (Extreme Learning Machine) - is a methodology for learning single-hidden layer feedforward neural networks. Unlike traditional neural networks ELM does not need any extra time to adjust weights or biases as it chooses them at random therefore providing a better performance in a short time.
Box theory – the price of the stocks generally oscillates in a certain range during a period of time named as the box. If the price breaks the upper boundary or the lower boundary of the oscillation box, it will enter another oscillation box in which the price will start a new lower or upward trend, respectively, indicating to us it’s time to buy or sell the stocks.
Gray Correlation Degree - The method is using the geometric shape of sequence curves to present the relational degree between two data sequences, i.e. it gives us a measure of the closeness of the curves calculated between the feature and the target.

The fundamental assumption of technical analysis holds that past performance can inform future movements. Constructing our input feature values such as Moving Average(MA), Rate of Change(ROC) and Relative Strength Index(RSI) from the existing features since each of its own adds the advantage that reduces risk and increases the likelihood of profit. 

In order to get the boundary in next few days through prediction the stock market time-series, the boundary in period few days can be used as features. In this system, we use the highest price and lowest price of the stock in the future n1(30) days as the upper boundary Upk and lower boundary Lowk. 

A bull market is a market that is on the rise and is economically sound, while a bear market is a market that is receding, where most stocks are declining in value.

# *ELM*

This method is essentially a single feedforward neural network; its structure consists of a single layer of hidden nodes, where the weights between inputs and hidden nodes are randomly assigned and remain constant during training and predicting phases. On the contrary, the weights that connect hidden nodes to outputs can be trained very fast. Experimental studies showed that ELMs can produce acceptable predictive performance and their computational cost is much lower than networks trained by the back-propagation algorithm.

Number of nodes in the hidden layer – 1000

Activation function – Sigmoid function, ReLu function

The extreme learning machine tries to minimize the empirical and structural error by adjusting the weights and biases. 

# *Trading Strategy*
The basic idea of this theory is that the stock price is always has a certain shock range in a period of time, thus it has a maximum and a minimum price during this time. Imaging there are two ends of a box—the upper boundary and the lower boundary, therefore an oscillation box. When the stock price close to the lower boundary it has the rising trend and on the contrary close to the upper boundary. Furthermore, the price will go into another box to start a new shock in a range after it breaks through the boundary. 

After predicting the upper and lower boundary, which are described as Upi and Lowi , in next n1 days after ith-day, we need to set a standard to detect whether the price series crossing the border.

The first thing is that the price is very close to the lower boundary of the new box, and the second thing is that the lower boundary of the new box is moved upward. Similarly, the price will close to the upper boundary of the new box and the upper boundary of the new box will move downward when it crosses the lower boundary. 

This strategy is proven to be more effective than the buy and hold strategy.

# *OSELM*

OS-ELM consists of two phases: initialization phases and sequential learning phase. 

Initialization phase: In initialization, basic ELM is used to train a SLFN with a small chunk of initial training data. 

Online sequential learning phase: In the online sequential learning phase, the output weights are updated whenever a new chunk of input data with Nk+1 training samples arrives. The short-term prediction performance of the OS-ELM can be further increased with the use of forgetting factor which lies between λ ∈ (0, 1].

The forgetting factor λ enables OS-ELM to continually forget the outdated input data in process of learning, to reduce their bad affection to the following learning. 


