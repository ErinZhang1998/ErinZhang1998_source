+++
title = "Week 4"
summaryTitle = "[master-thesis] Formulation Week 4"
postSummary = "Trying to build a simple website for annotation"
tags = [
    "fifth_year",
]
categories = [
    "fifth_year",
]
date = "2021-10-15"
+++

## Week View
| Wednesday | Thursday | [Friday](#oct-15-friday) | [Saturday](#oct-16-saturday) | [Sunday](#oct-17-sunday) | [Thursday](#oct-18-thursday) | [Thursday](#oct-19-thursday) |

## Oct-18-Tuesday

## Oct-18-Monday

Change my mind: we want to group by primitives. Each trajectory should be the drawing of a primitive. 

So everytime the user draws a primitive, 

## Oct-17-Sunday

Since the website looks bad right now, I want to make things more aligned and centered. Start anew! 

Top Row (30%): annotation instructions.
Bottom Row (70%): 3 rows
- Practice drawing board: the user should be able to practice using mouse the draw, since it is difficult.
- Actual recording drawing board: the same board but with all the start recording, done recording, next recording buttons.
- A list of primitives that the user can use.  

Tweaking every little alignment details... But I finally understood how margin and padding works in html... They do make things very easy to view.

Biggest decision: in the old drawing board code, they define each "ActionSet" as 1s of drawing on the board, so it connects all the points that are drawn in 1s. But we want to group actions differently: we want to group by strokes.

## Oct-16-Saturday

I was trying to use Hugo with javascript, but it seems easier to start with html?

Time to learn html, css, and JS! Thought I never need to touch front-end but here I am. 
- Simple tutorial to know what's going on: [🔗](https://docs.microsoft.com/en-us/learn/modules/build-simple-website/1-introduction)
- Some templates to organize the html page: [🔗](https://www.os-templates.com/free-basic-html5-templates?start=63)

Plan: instructions on the right, and drawing board on the left. \
List of primitives on the right. 

I am thinking we shouldn't show all the buttons at once. Like the user should only have the option to look at the "Record" button. How do I make the "Record" button colorful? Like red seems to be color used in iPhone recordings. --> Great effects of glowing, but seems distrcting, crossed out. 

{{< figure src="/images/master/week4/website_v1.png" height="400">}}

We need to have the primitives on there to limit the difficult of learning later on; I think there is already tons of variations in terms what a circle can be drawn.

(SVG requires calculation, and you can only have one svg tag in one html file...?)
{{< figure src="/images/master/week4/website_v1_primitive.png" height="400">}}

## Oct-15-Friday

Start thinking about the interface, I think there needs to be a drawing board, and we need to be able to track what the users have inputted and save it somwhere. 

Find the following resources: [🔗](http://ramkulkarni.com/blog/record-and-playback-drawing-in-html5-canvas/)

I will modify based on it.