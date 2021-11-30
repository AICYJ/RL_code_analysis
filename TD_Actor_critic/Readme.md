This code explain about TD actor critic.

We will explain with the assumption that we have studied policy gradient. Please refer to the below equation for the policy gradient equation.  

<p align="left"><img src="figure/policy_gradient.png" /></p>  

Briefly explaining the policy gradient equation, which was discussed in detail earlier, the equation &#8711;<sub>&theta;</sub>J(&theta;) can be said to calculate the loss value to learn the parameters of the deep learning model. &#8711;<sub>&theta;</sub> in the right equation is the amount of change in the reward value according to the parameters. &#960;<sub>&theta;</sub>(s,a) is policy Q<sub>&#960;<sub>&theta;</sub></sub>(s,a) is cumulative reward. If you don't understand this explanation well, please refer to the previous explaination.

<p align="left"><img src="figure/Advatage Actor-critic.png" /></p>

It is possible to derive an Advantage Actor-critic equation by using a policy gradient equation. In short, this was also derived by applying A<sub>&#960;<sub>&theta;</sub></sub>(s,a) ~ Q<sub>&#960;<sub>&theta;</sub></sub>(s,a)-V<sub>&#960;<sub>&theta;</sub></sub>(s). We will post the detailed proof later.

<p align="left"><img src="figure/TD_Ator_Critic.png" /></p>

The above equation is proved through &delta;=r+&gamma;V(s<sup>'</sup>)-V(s). As a result, we can use algorithms that can update policies with only n-step calculations and value-based functions. 
Based on this understanding, let's check the sample code.

thank you