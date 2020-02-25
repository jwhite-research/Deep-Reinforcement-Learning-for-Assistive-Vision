# Supplementary Material
This page displays the saliency and feature map videos referenced in the paper "Vision Processing for Assistive Vision: A Deep Reinforcement Learning Approach". The two videos shown below were rendered using single frames that were individually passed to the trained Deep Neural Network (DNN) and then collated to produce these videos. 

## Saliency Video:
Our saliency video was produced using the saliency algorithm by [Greydanus et al.](https://arxiv.org/abs/1711.00138)(https://github.com/greydanus/visualize_atari). On each single frame a saliency map is rendered that is then overlayed on the original grayscale image. Highlighted regions in the frames displayed in the video indicate areas of importance for the agent to make an action selection since saliency is based on the predicted policy output. A key outcome from this video is that the agent can dynamically make decisions based upon a rapidly changing context and the task it is presented with. Thus, images that are passed to the DNN are filtered and produce a policy output based on the context of the input image. Further, this video explains some of the agent's behaviour and its tendency to focus on certain features of particular importance for it to effectively navigate. In particular, the agent can be seen focusing areas with high levels of depth and edges at the wall-sky interface. However, regions of high depth are prioritised if the agent is planning on traversing toward that area of the maze as is made evident by the video below. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/ylgkQkxRAtY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Feature Map Video:

Each individual image when passed to the input layer DNN produces a set of filter responses from the trained convolutional layers. To further analyse the behaviour and critical features that facilitate the agent's ability to navigate, we present the following video. Here, we show 12 of the 16 feature maps that evolve frame-to-frame and individually outline a different optimised feature for the task setting. Each feature map is at a resolution of (21 x 21) down from an image input resolution of (84 x 84). We exclude 4 of the trained feature maps as they do not produce filter responses. It is likely that the 12 feature maps shown below were deemed sufficient to complete the task. Note that the set of features shown resemble those from hand-crafted approaches (e.g. plane detection, edge detection).

<iframe width="560" height="315" src="https://www.youtube.com/embed/9OCJqV4tCAg" frameborder="0" allow="accelerometer; autoplay; encrypted-media" allowfullscreen></iframe>

## Real Feature Map Video:

<iframe width="560" height="315" src="https://www.youtube.com/embed/m5rRO4TjyN0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
