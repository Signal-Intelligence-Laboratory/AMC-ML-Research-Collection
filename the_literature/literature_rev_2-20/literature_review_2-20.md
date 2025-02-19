# Literature Review and Model Structure Overview for 2/20/25

## Literature Review
### Review of Methods of Automatic Signal Classification in Wireless Systems
Focus on strengths and weaknesses of each method. Get to the why I'm starting with CNN (don't trust methods that treat signals as visuals, simple, still gets researched). Reinforce that this is not limiting the entire project to CNNs, just a starting off point. Both ML and stochastic can be measured here, the point is comparison. 

Remember: this all started with the question of what is the fasted method by which we can reverse-engineer a signal with nothing already known about it? Maybe it's ML, maybe it's stochastic, maybe a mix? We're going for speed, and a known signal when all is said and done. (In other words, if we can get away with a less accurate CNN but it's still faster than stochastic if we run it a couple times, does that work?)

### Review of Testing and Analysis of these Systems
My instinct here is that many groups have been only worried about accuracy recently. Or they're counteracting methods (like FGSM) which really are hard to accomplish outside of the simulation space. Why are we worried about methods with no practical application? General idea: let's do real world testing, and clearly compare with every metric we can come up with.


## Model Structure Overview

Block diagram of model goes here

Try to label each block with the possible methodologies which can fit the block, and why we might want to examine in study.

