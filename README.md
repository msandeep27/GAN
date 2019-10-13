GANs are made for. Generative Adversarial Networks belong to the set of generative models. It means that they are able to produce / to generate (we’ll see how) new content. To illustrate this notion of “generative models”, we can take a look at some well known examples of results obtained with GANs.


What’s so magic about GANs?

In short, they belong to the set of algorithms named generative models. These algorithms belong to the field of unsupervised learning, a sub-set of ML which aims to study algorithms that learn the underlying structure of the given data, without specifying a target value. Generative models learn the intrinsic distribution function of the input data p(x) (or p(x,y) if there are multiple targets/classes in the dataset), allowing them to generate both synthetic inputs x’ and outputs/targets y’, typically given some hidden parameters.
In contrast, supervised learning algorithms learn to map a function y’=f(x), given labeled data y. An example of this would be classification, where one could use customer purchase data (x) and the customer respective age (y) to classify new customers. Most of the supervised learning algorithms are inherently discriminative, which means they learn how to model the conditional probability distribution function (p.d.f) p(y|x) instead, which is the probability of a target (age=35) given an input (purchase=milk). Despite the fact that one could make predictions with this p.d.f, one is not allowed to sample new instances (simulate customers with ages) from the input distribution directly.
Side-note: It is possible to use discriminative algorithms which are not probabilistic, they are called discriminative functions.
GANs they have proven to be really succesfull in modeling and generating high dimensional data, which is why they’ve become so popular. Nevertheless they are not the only types of Generative Models, others include Variational Autoencoders (VAEs) and pixelCNN/pixelRNN and real NVP. Each model has its own tradeoffs.

Some of the most relevant GAN pros and cons for the are:
They currently generate the sharpest images
They are easy to train (since no statistical inference is required), and only back-propogation is needed to obtain gradients
GANs are difficult to optimize due to unstable training dynamics.

No statistical inference can be done with them (except here):
GANs belong to the class of direct implicit density models; they model p(x) without explicitly defining the p.d.f.
So.. why generative models?
Generative models are one of the most promising approaches to understand the vast amount of data that surrounds us nowadays. According to OpenAI, algorithms which are able to create data might be substantially better at understanding intrinsically the world. The idea that generative models hold a better potential at solving our problems can be illustrated using the quote of one of my favourite physicists.
“What I cannot create, I do not understand.” — Richard P. Feynman
(I strongly suggest reading his book “Surely You’re Joking Mr. Feynman”)
Generative models can be thought as containing more information than their discriminative counterpart/complement, since they also be used for discriminative tasks such as classification or regression (where the target is a continuous value such as ℝ). One could calculate the conditional p.d.f p(y|x) needed most of the times for such tasks, by using statistical inference on the joint p.d.f. p(x,y) if it is available in the generative model.

GAN Model

![Alt text](/images/GAN-Network.png?raw=true)

We used Fashion MNIST dataset to test GAN Model

![Alt text](/images/GAN-Images.png?raw=true)
