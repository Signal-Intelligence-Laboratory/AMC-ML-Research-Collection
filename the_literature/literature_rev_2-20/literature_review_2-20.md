# Literature Review and Model Structure Overview for 2/20/25

## Literature Review of Automatic Modulation Classification in Wireless Systems
There are two main questions in the determination of the approach I am choosing to take:
1. What is the benfit of a Machine Learning approach to Automatic Modulation Classification over a purely stochastic approach?
2. If it is assumed that there is *some* benefit derived from a Machine Learning approach, why one approach over another?

Beginning with question 1, we'll return to the initial research question which is along the lines of: "given an unknown wireless system, how quickly can we obtain enough information about the signal it outputs to demodulate and decode it?" Some of the challenges of this problem are as follows:
- We assume complete blindness, so the system should be extensible for as many wireless signal types as possible
- Knowledge of generic moduation type is not enough to demodulate higher order modulations (assuming HOM is in the problem scope)
- The proposed problem is real-world application. Simulated environments can assess precision in generalized randomness, however it is difficult for the to account for unnatural perturbations.
- Real world application also means that computational intensity should be minimized. 

There is research which seeks to address some of these questions. Perhaps the closest existing work to our proposed problem remains to be Universal Radio Hacker [[1](#references)]. URH can detect and classify binary ASK (and OOK), PSK, and FSK signals by pure signal processing, probabilistic variance calculations, and a decision tree. The algorithm is (relatively) computationally light, and requires no dataset. There are, however, limitations in the URH suite which come mostly in the form of complexity. URH cannot specifically detect HOMs of any of these base modulation schemes, and it is also limited to the three primary schemes listed previously. This was all addressed in the future work section of their paper. Also in this section, they reference a possible extension to include HOMs [[2](#references)] which is based on a wavelet transform-based neural network approach. I reached out to Andreas Noack of URH to ask if they had attempted to implement this, and he said that they had, but they found that the approach was too bulky for their intended use case. 

But we're assuming that we want to be able to demodulate *any* signal, which URH, as good as it is, cannot do natively. So now, we return to more generalized AMC research. The two most prevalent paths for HOM AMC are utilizing either cumulants [[3](#references)], or machine learning [[2, 4, 5, 6](#references)], or in rare cases, both [[5](#references)]. 

The main issue that I come across in many of these papers has to do with their comparisons of their own work against other methodologies. I did not have the time to go through all of the papers that I found to assess their assessments, though this could certainly be some future work. I believe I can, however, with some confidence, say that generally, papers utilizing machine learning will claim greater accuracy in generally more difficult (noisy, adversarial, etc.) environments over stochastic, or probabilistic methods, frequently referred to as "traditional methods". Now, depending on the metric chosen to measure by, this is often proven to be correct in their provided graphs. However, I think that some of these methods are short-sighted when it comes to what they are actually trying to solve. While they are perhaps improving their accuracy, I think there are some questions overlooked:
- Is there an upper limit on accuracy? (And I mean for the ML fix itself, it doesn't count if just general signal processing techniques are applied)
- Is the problem environment even useful outside of a simulation environment?
- What's the difference between 95% accuracy and 98% accuracy if I can just run the system again?
- Yes, we've increased the number of signal types we can detect, but how large of a database do we need to accomplish this?
- How small of a database can we use and still get decent results?

I have yet to find literature that addresses most of these questions, because this is not the focus of current research. Current research is geared towards improvement of the systems with very little questioning the systems themselves. The only research that I have found that does question the actual systems, is in adversarial models [[8, 9, 10](#references)]. Though these do not tend to answer my previous questions, they do at least address weaknesses of the system itself, which is its inherent property of decision making. However, to my knowledge, a wholesale, all aspects comparison and review of methods of AMC has yet to be conducted. 

The grander proposal of this project is to create an AMC system allowing for the use of multiple AMC methods with the intention of investigating system performance without the only end goal being accuracy. The intention is to observe what might make a realistically useful system, and by which methodologies this might be most effective.

In the short term, the proposal is to create a Convolutional Neural Network for AMC. It should first be able interact with both simulated and real-world signals such that its performance can be assessed in an actual application environment. It should also have easily variable parameters such as amount of training data, generation of said data, convolutional layers, and other elements of its construction to observe how its desired qualities such as speed and accuracy vary with tradeoffs in its construction. 

The CNN architecture was chosen for this first project for a few reasons. The first reason is my own skepticism of the methodology. There are a handful of ML AMC methods which function by first converting the detected signal into an image representation with the intention of then untilizing image classifiers to classify the signal. To me, the approach just reads as strange. First converting signal to image in order to classify seems like an unnecessary extra step which seems like it could be avoided if the signal were analyzed with purely signal processing techniques. There are variations which treat the signal as the 1-dimensional amplitude/time representation, but still, the system seems to forego analysis for a nonspecific do-it-all approach. I cast aspersions, but my instinct is that this method is chosen when research has more of an interest in the machine learning than the actual usefulness of their system in a wireless environment (see- [11](#references) for more issues in "Domain Expertise"). The second reason I chose this system is for ubiquity and simplicity (at least for me). I understand the general concept of convolution for feature detection, it's common in signal processing, it then has the additional step of training a neural network on top of it. Also, CNN deep learning solutions are not difficult to find in recent research, meaning that building off of existing systems will be less of a challenge. The CNN system is also only a starting point. Again, the large-scale goal is to try many of these systems, the CNN is just a place to begin the investigation.

## Model Structure Overview

[Model Diagram](AMC_General_Diagram.drawio.png)


## References
[1] [Automatic Modulation Parameter Detection In Practice](https://dl.acm.org/doi/pdf/10.1145/3375894.3375896)

[2] [Automatic Modulation Recognition Using Wavelet Transform and Neural Networks in Wireless Systems](https://asp-eurasipjournals.springeropen.com/articles/10.1155/2010/532898)

[3] [Automatic modulation classification based on high order cumulants and hierarchical polynomial classifiers](https://www.sciencedirect.com/science/article/abs/pii/S1874490716301094)

[4] [Deep Learning-Based Automatic Modulation Classification Using Robust CNN Architecture for Cognitive Radio Networks](https://www.mdpi.com/1424-8220/23/23/9467)

[5] [Modulation Classification Using Convolutional Neural Network Based Deep Learning Model](https://ieeexplore.ieee.org/document/7929000)

[6][Deep Learning for Robust and Secure Wireless Communications](https://link.springer.com/chapter/10.1007/978-3-031-53510-9_6)

[7] [Using Capsule Networks to Classify Digitally Modulated Signals with Raw I/Q Data](https://arxiv.org/pdf/2205.09287)

[8] [A Multiscale Discriminative Attack Method for Automatic Modulation Classification](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10793417)

[9] [The Threat of Adversarial Attacks Against Machine Learning in Network Security: A Survey](https://arxiv.org/pdf/1911.02621)

[10] [Defending AI-Based Automatic Modulation Recognition Models Against Adversarial Attacks](https://digitalcommons.odu.edu/cgi/viewcontent.cgi?article=1203&context=engtech_fac_pubs)

[11] [The Domain Expertise Trap](https://cyclostationary.blog/2022/04/21/the-domain-expertise-trap/)

