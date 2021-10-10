+++
title = "Week 3"
summaryTitle = "[master-thesis] Formulation Week 3"
postSummary = "This week, we started to zooming into the idea of children-drawings: single figures of cats, flowers, faces, houses that are made from simple basic `block`"
tags = [
    "fifth_year",
]
categories = [
    "fifth_year",
]
date = "2014-10-20"
+++

## Week View
| Wednesday | [Thursday](#oct-7-thursday) | [Friday](#oct-8-friday) | [Saturday](#oct-9-saturday) | [Sunday](#oct-10-sunday) | Monday | Tuesday |


## Oct-10 Sunday
[🔝](#week-view)

## Oct-9 Saturday
[🔝](#week-view)
### The big 3
I think I want to answer these 3 questions:
- What is the *very general* question that we want to solve?
    - e.g. pose estimation
- How to formulate this question as a formal research question?
    - What aspect of the problem mentioned in bulletin-1 that we want to tackle?
    - What baseline methods are we improving? 
- Which method are we using?
    - Architecture of the model?

*very general*: drawing...
(okay too general, pen drawing?) \
*imageined ideal product at the end*: 
> h: this is a "face" {{< figure src="/images/master/week3/face1.png" height="100">}} \
>>(point) this is the "inside of a face" \
>>(point) this is the "outside of a face" 

> r: okay

{{< figure src="/images/master/week3/ideal_situation_1.png">}}


*"user-defined"*: every human can have their own version of face or cat, it would be great if the robot can process generic input from anyone instead of just memorizing one way of drawing something. \
*"episodes"*: ➡️ hierarchical structure 
- start of an episode: "now I will teach you how to draw an eye" 
- during the episode: commands to create the face
- end of episode: forming the concept, categorize the concept (oh, another way of drawing eyes)

Few interesting ideas from SORNet[^1]
(talking in terms of how these ideas can help me answer the aforementioned 3 questions)

---
✅ multi-step robotics task. \
I think drawing is a multi-step robotics task. It is goal-oriented, because the goal of each episode is to, for example, draw the eye that the human wishes to teach the robot about. 

✅ represent spatial relationships between entities in the world. \
Of course, how the parts come together to form one drawing. 

---

## Oct-8 Friday
[🔝](#week-view)

🤔 segmentation, semantic segmentation, generative modeling \
The paper that Oliver showed me [📃](https://arxiv.org/abs/1903.07291). \
**?** learning a distribution of what a flower looks like, but the bulk of the work would been done in terms of generating pixel-images?

## Oct-7 Thursday
[🔝](#week-view)


[^1]: @misc{yuan2021sornet,
      title={SORNet: Spatial Object-Centric Representations for Sequential Manipulation}, 
      author={Wentao Yuan and Chris Paxton and Karthik Desingh and Dieter Fox},
      year={2021},
      eprint={2109.03891},
      archivePrefix={arXiv},
      primaryClass={cs.RO}
}


