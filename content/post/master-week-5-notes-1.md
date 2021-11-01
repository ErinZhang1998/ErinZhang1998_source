+++
title = "Week 5"
summaryTitle = "[master-thesis] Formulation Week 5"
postSummary = "First version of website works well, but want to make instructions more suitable for users so that we can use Amazon Turks."
tags = [
    "fifth_year",
]
categories = [
    "fifth_year",
]
date = "2021-10-20"
katex = true
+++

## Week View
| [Wednesday](#oct-20-wednesday) | Thursday | [Friday](#oct-22-friday) | [Saturday](#oct-23-saturday) | [Sunday](#oct-24-sunday) | [Monday](#oct-25-monday) | [Tuesday](#oct-26-tuesday) |

## Oct-25-Monday
- Finished the main annotation component on the webpage. Used table instead of row/div format so that we can easily have more than one prompt in a single annotation task. 
- Use "tooltips" to remind Turks the intended usage of a button.
    - Should not annotate a step if no drawing for that step is done.

{{< figure src="/images/master/week5/website-oct-25.png" height="300">}}

We will need exam questions for the qualification round.

Constantly thinking about the goal of this project: symbol grounding.

## Oct-24-Sunday
Design new Amazon Turk URL

Dynamically add new component tutorials: 
[🔗](https://makitweb.com/dynamically-add-and-remove-element-with-jquery/)

## Oct-23-Saturday
- First decide the format of the annotation task.
- A list of things that one annotation must contains.
- Come up with a list of requirements for the annotations.

## Oct-22-Friday

#### GMM vs. GAN
**GMM method** 
- Mixture of Factor Analyzers. \\(x_n\\) sample from \\(Az + \mu + \epsilon \\), where \\(A\\) is a matrix of dimension \\(d \times l \\).
- Maximize log likelihood of all samples. \\(\sum_{n}^N \sum_{i}^K \pi_{i} P(x_n | \mu_i, \Sigma_i) \\)

**Notes**
- New metrics to measure similarity of two distributions: intuition is decide if the difference between numbers of samples that fall into the same "bin" is statistically significant. \\(NDB = \frac{\text{number of different bins}}{K} \\)
- How to avoid the common mode collapse (failure to model the entire data distribution) problem in GANs? (Note: this paper is published in 2018, is mode collapse still a problem today? Maybe new efforts have mitigated the issues.)
    - GAN fails to model some bins (some parts of the distribution).
    - MFA components represent some prototypes, and the column vectors of the rectangular scale matrix \\(A\\) represent changes from the mean image. "The latent variable z controls the combination of column-vectors added to the mean image."
- GMMs capture the statistical structure for easy inference. 
    - Directly optimize for the log-likelihood. vs. It is difficult to calculate log-likelihood of heldout data for GANs. 
    - ❓ "First, since GANs by definition only output samples on a manifold within the high dimensional space, converting them into full probability models requires an arbitrary noise model. Second, calculating the log likelihood for a GAN requires integrating out the latent variable and this is intractable in high dimensions (although encouraging results have been obtained for smaller image sizes)".
    - Handling tasks like outlier detection and image inpainting.
- How to make GMMs generate sharp images?

GMM Tutorials
[🔗](https://jakevdp.github.io/PythonDataScienceHandbook/05.12-gaussian-mixtures.html)
[🔗](https://www.kernel-operations.io/keops/_auto_tutorials/gaussian_mixture/plot_gaussian_mixture.html#sphx-glr-download-auto-tutorials-gaussian-mixture-plot-gaussian-mixture-py)

**Relate to my project**
- What distribution are we modeling? It seems more like a mapping from language commands to 2D curves, but the model is not modeling the distribution of the entire sketch/drawing ("a cat") but a part of the drawing and how it relates to the whole: conditional distribution. "cat ears" --> [certain curve at certain location relation to "cat face"]

## Oct-20-Wednesday

- Questions about the "Next" button: ✅ Users label their own step. 🤔 What does each **step** incorporates? One step in the drawing = Draw one primitive, label what it means.
- Oliver, Yonatan, and I all think it is fine to move towards the directiof of less-constrained drawing, since we can always "fit" to the user drawings using SVG / PNG.  
- Do we still need the primitives? Would a decision make running baseline methods difficult? 
- How to design the qualification round before actual annotations?
- Axis-aligned vs. object-aligned bounding boxes? They can used for first decising where a component is.
- "What did you just draw? What does the component mean?"

Ask Yingshan about the Amazon Turk templates. \
Make decisions about what to modify so it is the Amazon-Turkable. \
Modify the current website according to the decisions. \
Publish on the mock-up Amazon website. \
Test out on friends. 