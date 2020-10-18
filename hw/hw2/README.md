# HW2

## Concepts
* MAML and ProtoNet implementation
* Effect of optimizing the inner-loop learning rate in MAML
* Effect of meta-test K (with a smaller meta-train K) between MAML and ProtoNet 

![MAML vs. ProtoNet](maml_vs_protonet_diagram.png "It's the support-set-conditioned model that differs between MAML and ProtoNet. Image credit: Chen et al 2019 (1904.04232)")

## Main takeaways:
* "Inner loop" = optimizing for the task at hand (traditional loop). "Outer loop" = optimizing to learn across tasks to be better prepared for the next new one (meta-learning loop).
* In optimization-based meta learning algorithms, you can learn the inner-loop learning rate because you embed a differentiable per-task optimization procedure in the meta-learning process. For MAML, you differentiate through the inner loop to get gradients of the final task loss with respect to the initial weights used in the inner loop. Similarly, you could compute the gradients of your final task loss w.r.t to the learning rate used in the inner loop. Note that you're only learning the inner-loop learning rate and not the outer learning rate.
