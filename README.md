# Lstm historical temp prediction Coursera Project Work

- Recurrent Neural Networks
Humans don’t start their thinking from scratch every second. As you read this essay, you understand each word based on your understanding of previous words. You don’t throw everything away and start thinking from scratch again. Your thoughts have persistence.

- Traditional neural networks can’t do this, and it seems like a major shortcoming. For example, imagine you want to classify what kind of event is happening at every point in a movie. It’s unclear how a traditional neural network could use its reasoning about previous events in the film to inform later ones.

- Recurrent neural networks address this issue. They are networks with loops in them, allowing information to persist.

## The Problem of Long-Term Dependencies

1. One of the appeals of RNNs is the idea that they might be able to connect previous information to the present task, such as using previous video frames might inform the understanding of the present frame. If RNNs could do this, they’d be extremely useful. But can they? It depends.

2. Sometimes, we only need to look at recent information to perform the present task. For example, consider a language model trying to predict the next word based on the previous ones. If we are trying to predict the last word in “the clouds are in the sky,” we don’t need any further context – it’s pretty obvious the next word is going to be sky. In such cases, where the gap between the relevant information and the place that it’s needed is small, RNNs can learn to use the past information.

3. But there are also cases where we need more context. Consider trying to predict the last word in the text “I grew up in France… I speak fluent French.” Recent information suggests that the next word is probably the name of a language, but if we want to narrow down which language, we need the context of France, from further back. It’s entirely possible for the gap between the relevant information and the point where it is needed to become very large.

## LSTM Networks
Long Short Term Memory networks – usually just called “LSTMs” – are a special kind of RNN, capable of learning long-term dependencies. They were introduced by Hochreiter & Schmidhuber (1997), and were refined and popularized by many people in following work.1 They work tremendously well on a large variety of problems, and are now widely used.

- LSTMs are explicitly designed to avoid the long-term dependency problem. Remembering information for long periods of time is practically their default behavior, not something they struggle to learn!

- All recurrent neural networks have the form of a chain of repeating modules of neural network. In standard RNNs, this repeating module will have a very simple structure, such as a single tanh layer.
reference- https://colah.github.io/posts/2015-08-Understanding-LSTMs/





![image](https://user-images.githubusercontent.com/70902291/123842688-b0a10e00-d92e-11eb-8e44-62d01fa08a78.png)


![image](https://user-images.githubusercontent.com/70902291/123842781-ca425580-d92e-11eb-864e-fa1a14012f99.png)

![image](https://user-images.githubusercontent.com/70902291/123842816-d4fcea80-d92e-11eb-898e-9f649fa254ed.png)

![image](https://user-images.githubusercontent.com/70902291/123842836-da5a3500-d92e-11eb-884b-5c3a1e7fd394.png)

![image](https://user-images.githubusercontent.com/70902291/123842865-e0501600-d92e-11eb-9e08-4fdf70012d0e.png)

![image](https://user-images.githubusercontent.com/70902291/123842894-e5ad6080-d92e-11eb-80c3-0c485188c201.png)

![image](https://user-images.githubusercontent.com/70902291/123842949-f52ca980-d92e-11eb-922e-44514350e32a.png)
reference- coursera project
