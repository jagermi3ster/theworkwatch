---
title: The Watchers' Group Review Ticket
layout: default
description: In this ticket, we discuss what we completed in the past week, our planning process, what problems we faced and what we still have left to do.
toc: true
permalink: /watchersreviewticket
---

# Project Overview

The Work Watch is an interactive, customizable stopwatch program which helps you organize your work sessions. Though we provide default recommendations for break intervals, duration, and timer notification intervals, the user can customize them fully. The user is also able to create a list of tasks to complete during the work session, along with their expected duration.

The user is notified when it is time to take a break and when they had anticipated they would have completed a certain task to help keep them on track.

## Planning

Though not ideal with their format due to a lack of checkboxes (as mentioned in class), up to this point, our group has used an issue on our group Flask Github repository to organize assignments for each week as well as what we intend to get done. See the full SCRUM board [here](https://github.com/drewreed2005/The-Watchers/issues/1).

From the first week, we laid out the features we wanted to include (plus some bonuses) and left placeholders for when we completed them/were actively working on them. As can be seen by looking week by week, we mostly tried to complete things in the order that they are listed.

In the "Goals" section of the SCRUM Board table, we outlined our interests for the next week of work. At the beginning of each week, we looked back at these goals and referenced them when creating a sprint plan, reflected by the "Assignments" each week given to various roles. Sometimes the assignments are more specific than other times. It depends on what specifically we saw necessary to get done by the end of the day.

## What We've Completed in the Past Week

It would probably be most efficient to explain what we've done in the past week by looking at [this page](https://jagermi3ster.github.io/theworkwatch/workwatchbeta).

At the beginning of this week, the CSS design work for the timer elements was a bit more than half done thanks to Jagger, and it gave us a strong framework for this week. Drew's work converting the Python stopwatch code to nearly identical Javascript made the process of converting our old backend into applicable Javascript code.

Every group member found this week to be a dedicated lesson in HTML, CSS and Javascript, as even our backend developer Devon joined in on frontend until we were able to get our API back up and working (more on that later).

We discussed how we'd implement various elements as a group until coming to a consensus and having one or two of us code the necessary functions while the others went to work finding other things to work on simultaneously.

This week, starting from just a styled HTML page and some disconnected stopwatch Javascript code, we managed to complete...
- Making "Break," "Notification," and "Task" menus appear when corresponding buttons are clicked
- Making input windows with restricted possible values in each menu (and a robust system to check for/correct invalid inputs)
- Creating a "Hide/Show Timer" button that makes it invisible (and the button's label itself changes based on whether or not it is already hidden)
- A second-based stopwatch attached to formerly-created HTML code
- A break time mechanic in which the timer keeps running, but the expected task duration is extended to account for the break
- A "Start" button that checks for the settings input in the menus and instructs the user when an invalid input was provided (and only runs its code when the timer is *not* running; some code references disregarded this and clicking "Start" repeatedly made the timer rapidly speed up)
- A "Stop" button that simply stops the uptick of time
- A "Reset" button that completely resets all time variables and tasks
- A notification box which lets the user know vaguely how long the timer has run (for users with hidden timers), when it is and is not break time, and when they have spend more time than expected on a task.
- A "Task Complete" button which sends the user to the next task in their list when pressed or, if it's their last task, resets the timer and provides a reflection on the work session.
- A task box with a maximum of five possible tasks (data appended into lists with the "Add Task to Tasklist" button) to be displayed
- A reflection system which points out which tasks were completed early and which were completed late (also in task box)
- Overall redesigned and increased on the content we considered including at first

There is likely more that we neglected to mention.

## Problems We Faced and Solutions

Here are just a few off the top of our heads, expressed in a table.

<table>
    <tr>
        <td>Problem</td>
        <td>Solution</td>
    </tr>
    <tr>
        <td>Clicking the "Start" button while the timer was running allowed the user to significantly increase the timer's speed</td>
        <td>A new variable has been created to represent whether or not the timer is already running and the "Start" button only works when it is not running</td>
    </tr>
    <tr>
        <td>The constant variable which detects how long the timer has been running overall (since the sec, min and hr variables are all for the display) ran in centiseconds while the time input values are in minutes</td>
        <td>Time input variables are multiplied by 6000 before computation in most cases</td>
    </tr>
    <tr>
        <td>The break time did not lengthen the interval between when a task was anticipated to have been completed and when it was first started</td>
        <td>The time that a task is expected to be completed is represented by a "taskend" variable. If a break occurs in the middle of a task, the break duration variable is addded to the taskend variable to extend it</td>
    </tr>
    <tr>
        <td>Time input boxes did not prevent decimal inputs, which could mess up our time reading code</td>
        <td>When "Start" is pressed, a process has been added to verify that the time input is valid (between 1 and 999 minutes; decimals are rounded to the nearest integer). Invalid inputs prevent the stopwatch from starting, and instructions on how to fix them are provided in the notification box</td>
    </tr>
    <tr>
        <td>The "New Task" button in the task menu was supposed to concatenate a new set of input boxes (with different IDs) below the original and place the same button right below. The input boxes worked and the button still recognized its ID, but after the first press, it no longer functioned.</td>
        <td>Instead of cluttering up the menu, a new "task box" has been added at the bottom. The "New Task" button has been replaced with a "Add Task to Tasklist" button, which takes the data in the input boxes and creates a task with the corresponding values</td>
    </tr>
</table>

## What's Left to Do

We plan to add...

- A fetch process to our Alarm API that determines which alarm will play when a break occurs, ends, or a task was anticipated to have ended
- The location of the input windows for breaks, notifications and tasks will be relative to the corresponding button (rather than transforming and translating with pixels or percentage)

We've got a few days to figure it out, so everything should be great by the due date.