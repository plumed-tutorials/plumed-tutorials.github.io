# Reproducibility and extendibility

There has been a lot of discussion recently about ensuring that the calculations in papers are reproducible.
Our contribution to this discussion has been to introduce the PLUMED nest. Although I think all this effort is admirable,
I have a slight concern: __researchers rarely try to reproduce the work of their colleagues.__ A paper
that reproduces the calculations in another article would likely not be accepted in any reputable journal.
Why, then, are we trying to ensure others can reproduce the work that we have done?

The obvious answer is that if I can reproduce what another researcher has done, I can do new work that builds upon previous results.
However, I can only build upon what that previous researcher has done if I understand why the calculation was done in the way that was described.
Given this fact providing instructions that only explain the steps that were followed is not ideal. There is a danger
that someone reproducing the previous work will uncritically follow the previous researchers' steps. In doing so, they will not stop to reflect
on the steps that were taken and will be unable to work out how to apply the ideas from that earlier work in their own context.

We should consider the examples in the PLUMED nest as a rich set of model uses for PLUMED. We should
use these examples in the manual. As we do this, however, it may also be time to rethink the purpose of the manual. I have been 
developing code to annotate the examples in the nest using the manual. This is why I have spent time developing code that makes each keyword in the example inputs a tooltip.
I am trying to provide the documentation in a form that allows learners to start to understand how PLUMED works starting from any input, as I think this is how
students learn to use the code.

To put this another way, students are given some example input to run when they join research groups. They need to work out what these inputs are doing using the manual to understand what they are doing.
I want the nest to offer a mechanism for helping them through that process by providing tools (like the tooltips) for exploring the documentation in the context of the inputs in the nest.

When redeveloping all the modules I have developed over the last few years, I focus on clarity of documentation rather
than speed. In doing so, I routinely use a mechanism that uses shortcut actions that are replaced by multiple (simpler) actions during startup. I hope this allows students to see how complex
CVs such as Q6 are calculated, and how the calculation of these quantities can be extended. Furthermore, when they need something more computationally efficient, clear
documentation on how CVs are calculated will help them write code that runs on the particular architecture they are using.

To summarise, I hope the nest, documentation and so on ensure extendibility rather than reproducibility. In the grand scheme of things ensuring users can use PLUMED to do new things is far more important
than ensuring they can use it to reproduce work that others have already done.
