# Automatic Modulation Classification Research List

## ML Versus "Standard Models"
[RF Signal Classification with Synthetic Training Data and its Real-World Performance](https://arxiv.org/pdf/2206.12967)
- Cool paper on considering how effective synthetic training really is 

[Using Capsule Networks to Classify Digitally Modulated Signals with Raw I/Q Data](https://arxiv.org/pdf/2205.09287)
- Chad Spooner and ODU on use of Capsule networks over CNNs and RESNET
- There are more collaboration papers with similar work, though with a focus on cyclic cumulants

## Using Neural Networks
[Automatic Modulation Recognition Using Wavelet Transform and Neural Networks in Wireless Systems](https://asp-eurasipjournals.springeropen.com/articles/10.1155/2010/532898)
- Referenced by the authors of URH
- URH only works for binary modulation parameters. This was their intended method to expand to HOM
- Reached out to Andreas Noack of URH, he said they tried to implement, too bulky for their use case
- **Revisit the wavelet transform. It gets used here, but I haven't seen in other papers**
- Uses an **Artificial** Neural Network

[Using Sequence to Sequence Learning for Digital BPSK and QPSK Demodulation](https://strathprints.strath.ac.uk/63954/1/Kalade_etal_5GWF2018_Using_sequence_to_sequence_learning_for_digital_BPSK.pdf)
- Uses a **Recurrent** Neural Network
- Uses entirely simulation of physical layer. Not implemented on physical equipment.

[A Survey on Machine-Learning Techniques in Cognitive Radios](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6336689)
- Solid overview on other literature
- Covers ANNs in depth as well as other models
- Any comparison is purely theoretic

### Specifically CNNs / Deep Learning
[Deep Learning-Based Automatic Modulation Classification Using Robust CNN Architecture for Cognitive Radio Networks](https://www.mdpi.com/1424-8220/23/23/9467)

[Modulation Classification Using Convolutional Neural Network Based Deep Learning Model](https://ieeexplore.ieee.org/document/7929000)

[Deep Learning for Robust and Secure Wireless Communications](https://link.springer.com/chapter/10.1007/978-3-031-53510-9_6)
- Chapter written by Northeastern researchers who did work on JaX

[PhyDNNs: Bringing Deep Neural Networks to the Physical Layer](https://mentis.info/wp-content/uploads/2025/01/PhyDNNs_INFOCOM_2025.pdf)
- A bit confusing in what exactly the authors are changing
- Requires further reading

## Stochastic Processes
[Automatic Modulation Parameter Detection In Practice](https://dl.acm.org/doi/pdf/10.1145/3375894.3375896)
- Paper from URH. Uses a decision tree with probabilistic variance
- Lightweight and quick
- Meant for real-world application. Tested on real signals


