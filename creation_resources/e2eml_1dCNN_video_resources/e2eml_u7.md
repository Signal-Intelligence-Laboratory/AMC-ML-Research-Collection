# Unit 7 - Advanced model tuning

### 7.1 Hard max operator and classification
*No additional notes*

### 7.2 Confusion matrices, precision, and recall
*No additional notes*

### 7.3 Cottonwood code for HardMax and ConfusionLogger
For this walkthrough, make sure you are up to date, using the v23 tag

`git checkout v23`

You can follow along with the code walkthrough in core/blocks/operations.py

https://gitlab.com/brohrer/cottonwood/-/blob/v23/cottonwood/core/blocks/operations.py

and core/logger.py

https://gitlab.com/brohrer/cottonwood/-/blob/v23/cottonwood/core/logger.py

### 7.4 Tune classifier using mean precision
The model described in this lesson is the Mark 8 model in heartbeat_classifier_mark_8.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/heartbeat_classifier_mark_8.py

### 7.5 Add a second convolution layer
The Mark 9 model with two convolutional layers is in heartbeat_classifier_mark_9.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/heartbeat_classifier_mark_9.py

### 7.6 Layer-by-layer learning rates
The Mark 10 model incorporates layer-by-layer learning rates heartbeat_classifier_mark_10.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/heartbeat_classifier_mark_10.py

### 7.7 Add a second data channel
The Mark 12 model includes the second data channel heartbeat_classifier_mark_12.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/heartbeat_classifier_mark_12.py

The data loader and data blocks for the two-channel input are in

ecg_data_loader_2.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_loader_2.py

and ecg_data_block_2.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_block_2.py


And for the curious, here's [the paper on The Lottery Ticket Hypothesis](https://arxiv.org/abs/1803.03635) we reference in this lesson.

### 7.8 Augment the data with its derivatives
The Mark 13 model containing the the two channel inputs and their derivatives are in heartbeat_classifier_mark_13.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/heartbeat_classifier_mark_13.py

The data loader and data blocks for the derivative-enriched data are in

ecg_data_loader_d.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_loader_d.py

and ecg_data_block_d.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_block_d.py


For a side-track into calculating rates of change, check out this post.

https://e2eml.school/rate_of_change.html