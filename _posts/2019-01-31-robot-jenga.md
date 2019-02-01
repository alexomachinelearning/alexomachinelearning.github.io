---
layout: post
title: "Robot Jenga"
date:   2019-01-31 12:00:00 -0800

---
[Out of MIT](http://news.mit.edu/2019/robot-jenga-0130) came news yesterday of a successful experiment, of a robot arm that can learn to play Jenga on its own, and quickly.

The innovation appears to be in letting the robot arm's computing system learn in a way similar to the human approach, which is "try things out and see what happens, then assess". This is in opposition to feeding the computing system a high volume of training data and running simulations prior to trying things out.

Especially interesting to me is that the system integrates tactile information from the arm pushing the pieces and visual information from the camera. I'd like to learn how, if at all, the data is integrated as happens in a human brain structure like the thalamus.

I do wonder if the math of Jenga movements is fairly straightforward, making this experiment possible due to the symmetric nature of both the individual rectangular pieces and the vertical rectangular shape of the Jenga tower. This creates symmetries and a simplicity of physics that isn't found in very many games. For example, a starting Jenga tower stays a tower only to a modest tolerable level of surface incline; if the table surface isn't sufficiently level, the tower will fall over on itself and the training process can't proceed. So the starting conditions for the robot to learn from are fairly constrained by the geometric properties of the game's physical rules, which might in turn conserve the range of mathematical variables the training process has to take into account to an unusually small degree, making such rapid prediction-learning possible.

This is not to say the experiment isn't amazing but to wonder how transferable the machine learning conducted here will be to other contexts and tasks where symmetry is inexact.
