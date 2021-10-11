+++
title = "Embodiment Reading 1"
summaryTitle = "[reading] NLP"
postSummary = "About embodiment"
tags = [
    "reading_list",
    "cs_reading",
    "reading_embodiment",
]
categories = [
    "reading_list",
    "cs_reading",
]
date = "2020-04-01"
+++

* compositional language: "Move a rattling container from the lounge by the conference room to Bob’s office " ✅
* objects identified by physical properties ❌


> enable robots in human environments to adapt dynamically, continually learning new language constructions and perceptual concepts 

✅ yes..

> translating natural language commands to discrete robot actions 

best for drawing if continuous

> leverages conversations with humans to expand an initially low-resource, hand-crafted language understanding pipeline to reach better common ground with its human partners \
> with an **active learning approach** for acquiring such concepts [🔗](http://proceedings.mlr.press/v78/thomason17a/thomason17a.pdf) ... The system is initialized with a small seed of natural language data for semantic parsing, and no initial labels **tying concept words to physical objects**, instead learning parsing and grounding as needed through human-robot dialog

interesting..

> **Semantic parsing** has been used as a language understanding step in tasks involving unconstrained natural language instruction. \
> to tie language to planning

learning a general concept instead of memorization 

> Mapping from a **referring expression** such as the red cup to a **referent** in the world is an example of the symbol grounding problem 

>  In this work, we explicitly model **perceptual predicates** that refer to visual (e.g., red), audio (e.g., rattling), and haptic properties (e.g., full) of a fixed set of objects

visual: smaller curve, bigger curve, filled circle, empty circle... \
SMALL(CURVE(x))

**How to do perceptual grounding using interactions with humans?**
- Eye spy: Improving vision through dialog
- Grounding the meaning of words through vision and interactive gameplay
- Learning multi-modal grounded linguistic semantics by playing “I spy”
- Visual curiosity: Learning to ask questions to learn visual recognition
- Incrementally learning semantic attributes through dialogue interaction

>  To our knowledge, there is no existing end-to-end, grounded dialog agent with multi-modal perception against which to compare, and we instead ablate our model during evaluation

**Is this what I want: task-driven grounded dialog agent that fulfills natural language requests?**

> ❓ formal integration into the agent’s parsing pipeline. This allows, for example, the agent to use the meaning of known word take for unseen word grab at inference time.

> The grounding component takes in a **semantic meaning** representation and infers denotations and associated confidence values. \
> The same semantic meaning can ground differently depending on the environment. 

"environment" = different faces drawn on the paper 

> Feature representations of objects are connected to language labels by learning discriminative classifiers for each concept using the methods described in previous work [^31], [^37]. \
> In short, each concept is represented as an ensemble of classifiers over behavior-modality spaces weighted according to accuracy on available data (so yellow weighs look-vision highly, while rattle weighs drop-audio highly). While the objects have already been explored (i.e., they have feature representations), language labels must be gathered on the fly from human users to connect these features to words. \
> **Different predicates afford the agent different certainties** \ 
> perceptual concept models \
> **multiple possible groundings for ambiguous utterances** \
>  we associate a confidence distribution with the possible groundings for a semantic parse \

"red" --> (perceptual concept models) --> decision and a confidence value, 🟥 ? \
"the office" = "the eye"

---

"grab the silver can for alice"

> The agent maintains a **belief state** modeling the unobserved true task in the user’s mind

"(draw) a face with cute eyes"

---

Not sure: What is a concept model?
Not sure: how the updates are done on the concept model?


[^31]: Learning multi-modal grounded linguistic semantics by playing “I spy"
[^37]: Learning relational object categories using behavioral exploration and multimodal perception