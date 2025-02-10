# Unit 8 - Putting it all together

### 8.1 Fail loudly
In this lesson we walk through the discovery and repair of a bug. (Yikes!)

Make sure to checkout the version of Cottonwood with the bug fix.

`git checkout v24`

The bug was in line 273 of core/blocks/conv1d.py if you want to follow along.

https://gitlab.com/brohrer/cottonwood/-/blob/main/cottonwood/core/blocks/conv1d.py#L273

### 8.2 Train and evaluate the finished model
The module we walk through, heartbeat_classifier_mark_14.py, is here:

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/heartbeat_classifier_mark_14.py

### 8.3 Visualize the results (v1)
In this lesson we'll be walking through ecg_viz_mark_1.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_viz_mark_1.py

and heartbeat_classifier_demo.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/heartbeat_classifier_demo.py

### 8.4 Inspect the results (v1)
*No additional notes*

### 8.5 Augment the input (v2)
In this lesson we re-run the final training of the model using the augmented inputs. Most of these files have only trivial changes compared to earlier versions, but I created new files out of them so that there wouldn't be confusion over the changed versions.


ecg_data_loader_aug.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_loader_aug.py

ecg_data_block_aug.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_data_block_aug.py

heartbeat_classifier_mark_15.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/heartbeat_classifier_mark_15.py

heartbeat_classifier_demo_aug.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/heartbeat_classifier_demo_aug.py

ecg_viz_mark_2.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_viz_mark_2.py

### 8.6 Filter the classification results (v3)
The visualization upgrade is in ecg_viz_mark_3.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_viz_mark_3.py

### 8.7 Polish the visualization (v4)
The final round of visualization changes are in ecg_viz_mark_4.py

https://gitlab.com/brohrer/e2eml-course-321/-/blob/master/ecg_viz_mark_4.py

### 8.8 Weaknesses and strengths of our classifier
*No additional notes*

### 8.9 Wrap up
*No additional notes*

