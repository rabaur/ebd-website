---
layout: exercise
title: Exercise 3
date:   2024-02-14 15:48:01 +0100
categories: jekyll update
publish: true
---

# Exercise 3: Comparing Users’ Wayfinding across Hospital Typologies

## Submission Details 
- **Group size**: 2 students
- **Research question submission date:** 07.05.2025, 12:00 CET (via email)
- **Submission date**: 14.05.2025, 17:59 CET
- **Presentation date**: 14.05.2025
- **Submission materials**: 
	- For all the following materials, use the naming convention of your group member's last name delimited by `_`. Example: If your group consists of _A. Einstein_, _M. Curie_ → `einstein_curie` with the appropriate file extension.
	- The research question with experiment design. Send via Email to yiqwang@student.ethz.ch
	- The `fbx` models of the **two** hospital typologies. [Upload link](https://polybox.ethz.ch/index.php/s/9TXZpiYXYCgiqaX)
	- A presentation on this exercise (max. 10 minutes). [Upload link](https://polybox.ethz.ch/index.php/s/qwWBbx4C4SQyk74)
	- The `zip` compressed Unity project folder. [Upload link](https://polybox.ethz.ch/index.php/s/oknfDDjnzaLbZyH)

## Overview

This exercise is a continuation of exercise 2, where you analyzed spatial layouts and applied interventions based on metrics like YTI or SCI.

In this exercise, you will:
- Reflect the metrics, methods or results you worked with in task 2.
- Formulate a research question based on that reflection.
- Design & run a controlled virtual walkthrough experiment in Unity
- Collect & analyze navigation data (errors, time, paths, etc.) to answer your question.

You may validate or challenge your previous design interventions using wayfinding behavior. You may also explore the limitations of metric-driven design in predicting wayfinding performance. However, you are welcome to develop other research questions regarding wayfinding in hospitals.

The walkthrough experiment will take place in a desktop-based virtual environment created in Unity. Certain participant behavior during the walkthrough will be automatically tracked using a tool introduced in the course. As a general guide for the task, please refer to the tutorial given in week 11.


## 1 Creating 3D Geometry from Line Drawings
- Take a screenshot of the base layout and the intervention layout in [arxitect](https://arxitect.ivia.ch/home).
- Retrace the line drawings in your favourite 3D software. Note that we will only be able to assist you if you use [Rhino 7](https://www.rhino3d.com/download/archive/rhino/7/latest/)
  - If you decide to use Rhino 7, we can provide you with a license. Please send an email to [bopanb@student.ethz.ch](bopanb@student.ethz.ch) with the email that is associated with your Rhino account such that we can invite you to the license pool.
- Follow the approach shown in [the lecture](https://polybox.ethz.ch/index.php/s/KJyDGntA3wCwbrj) to properly scale your reference image, trace the lines, and create 3D walls from them.
- After this is done, follow the approach in the lecture to make sure that your walls are double-sided (adding thickness)
- You would like to categorize geometries into different layers, to later distinguish them in the eye-tracking results.
- Finally, export your geometry to `fbx`.

## 2 Importing Your 3D Geometry into Unity
- Follow [the lecture](https://polybox.ethz.ch/index.php/s/KJyDGntA3wCwbrj) and or [this tutorial](https://github.com/rabaur/EBD-Toolkit/tree/main) to obtain **GitHub Desktop**, **Unity 2022.3.XXX**, and the **Unity Project**.
- Familiarize with the functionalities of the tool through [the lecture](https://polybox.ethz.ch/index.php/s/KJyDGntA3wCwbrj).
- Make sure that you are able to collect and visualize some data in the reference scene `VirtualWalkthrough`.
- For more in-depth information, follow [this tutorial](https://github.com/rabaur/EBD-Toolkit/blob/main/docs/virtual_walkthrough.md)
- Go through this checklist before continuing with your next steps:
	- Have I imported my two layouts (the `fbx` files generated in step 2) into a new scene each (not the reference scene)?
	- Is my geometry up to scale?
	- Have I pressed "Calculate colliders" and applied the changes when importing the geometry?
	- Have I made all items static by clicking the "static" checkbox?
	- Have I assigned all objects to the relevant layers or created new layers if needed?
	- Have I rebuilt and visualized the `NavMesh`?

## 3 Coming Up With an Experiment
- For this exercise, you will be recruiting at least **6 participants** to perform the virtual walkthrough.
- These participants can be anyone except your group members themselves. They could also be colleagues from other EBD groups.
- Familiarize yourself with the outputs that the tool provides. What would be an interesting research question to ask in your layout? Consult [the lecture](https://polybox.ethz.ch/index.php/s/KJyDGntA3wCwbrj) to check what the properties of a good research question are.
- Your will perform a [within-subject](https://www.scribbr.com/methodology/within-subjects-design/) study, meaning all your participants will see both layouts. Randomize the order of experiments to combat learning effects.
- Define your research question, research variables and hypothesis. Example:
	- Question: does plan’s network efficiency affect the targeted wayfinding efficiency?
	- Independent variable: ICD value; dependent variable: wayfinding duration
	- Hypothesis: The doctors will on average take longer to find the patient room in layout 1 since the network efficiency is lower.
- Design an experiment environment in Unity to compare the change of your dependent variable by varying the independent variables.
	- Make sure that the studied variable can be directly measured. For example, wayfinding difficulty is represented by the path length or walkthrough duration, which is recorded by the tool in Unity.
	- Either control or record all irrelevant variables. For example, the participant’s input device should be kept the same, and the gaming experience should be recorded through tests or via questionnaire.
- Define a role and a task for your participant. Example:
	- Role: A new assistant doctor on the search for a patient.
	- Task: Start at the nurse station. The doctor needs to perform an undirected search, since it is their first working day.
- To support the hypothesis, you might need to collect data that are not directly available from the environment or the tool. Common techniques include but are not restricted to:
	- **A questionnaire** can reflect how the participant subjectively evaluate their wayfinding ability before the experiment, or precepted difficulty afterwards.
	- Asking the participant to **“think aloud”** could reveal navigation reasoning process and identify key spatial features or navigation strategies.
	- **A sketch map** reflects the memorization to the environment and test if the participant only finds the target by chance.
- **Important**: Before beginning with the experiments, send an email to [yiqwang@student.ethz.ch](mailto:yiqwang@student.ethz.ch) to submit your research question / hypothesis, your role, task, and how you will measure whether your hypothesis holds or not.
- Go through this checklist before continuing with the experiments:
	- I have recruited at least 6 participants
	- I have received a feedback regarding my experimental design

## 4 Analyzing and Visualizing the Outcomes
- Use the various visualization tools of the toolkit to visualize "visual attention" patterns and trajectories (at least one, both only if applicable to your hypothesis)
- Perform a statistical test on your collected outcomes. Google Sheets supports simple (and complex) statistical tests like a [t-Test](https://support.google.com/docs/answer/6055837?hl=en)
- Feel free to use more involved statistical tests or methods if applicable. You can find other types of statistical tests within the lecture slides or through online sources. Be aware of the applicability of these tests – they might only work with certain data types.


## 5 Presentation of results
Finally, summarize your experiment within a 10-minute presentation. It should at least include the following sections:
- What is your research question and what are the key variables? What is your hypothesis? Does your result support your hypothesis?
- How do you design your environment to control other irrelevant variables? What data did you collect?
- What is the main conclusion of the experiment? Do you have other interesting findings that worth deeper research?
- What difficulties did you face during the task? What could be the limitations of your study?
