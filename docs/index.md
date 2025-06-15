---
title: "CMU 05-332/632: Assistive Technology and Accessibility"
hide:
  - navigation
---


# CMU 05-332/632: Assistive Technology and Accessibility

## Instructors and Logistics

**Canvas:** [https://canvas.cmu.edu/courses/47948](https://canvas.cmu.edu/courses/47948)  
**Semester:** Fall 2025  
**Instructors:** [Patrick Carrington](https://www.patrickcarrington.com) (Office Hours: [By Appointment](https://www.calendly.com/patrickcarrington/officehours), 407 S. Craig St. Room 201)    
**Meeting Time:** Monday / Wednesday 11:00 AM to 12:20 PM  
**Location:** GHC 4215  



## Overview
This course will explore ability, disability, and accessibility. It introduces students to the theory, history, policy, and practice of accessibility and inclusion in computing. Course readings will explore relevant concepts from disability studies, accessibility, human-computer interaction, and design methods. Most accessibility content focuses on web accessibility for people who are blind or low-vision. In addition, through this course, you will learn how to design for people with different abilities including hearing loss, motor impairments, cognitive decline, and neurodiversity. As early adopters, people with disabilities have inspired a host of future user interface technologies, e.g., conversational assistants, text-to-speech, speech recognition, optical character recognition, predictive typing, tactile displays, etc. People with disabilities continue to be the first users of interface next-generation technologies that are gradually adopted widely. We will discuss how to design online and offline; how to design for visible and invisible disabilities; and how to design for permanent, situational, and temporary disabilities.

## Schedule and Readings

<div id="schedule" markdown>

<!-- Loading in schedule from schedule.yaml -->

{%- set schedule = extra.schedule -%}

{% if schedule %}
{% set ns = namespace(recitation_days_left=0, homework_days_left=0) %}

<table>
    <thead>
        <th><b>Date</b></th>
        <th><b>Lecture</b></th>
        <th><b>Readings</b></th>
        <th><b>Assignments</b></th>
    </thead>
    <tbody>
        {% for schedule_day in schedule %}
        <tr>
            <td><span class="schedule-day">{{schedule_day.date}}</span></td>

            <td><span class="schedule-lecture">
                {% if schedule_day.lecture.name != "" and schedule_day.lecture.link != "" %}
                    <a class="label label-red" href="{{schedule_day.lecture.link}}" target="_blank">
                        {{schedule_day.lecture.name}}
                    </a>
                {% elif schedule_day.lecture.name != "" %}
                    <b>{{schedule_day.lecture.name}}</b>
                {% endif %}
            </span></td>

            <td><span class="schedule-reading">
                {% if schedule_day.readings != "" %}
                    {% for reading in schedule_day.readings %}
                        {% if reading.name != "" %}
                            <a class="label label-blue" href="{{reading.link}}" target="_blank">
                            {{reading.name}}
                            </a><br/>
                        {% endif %}
                    {% endfor %}
                {% endif %}
            </span></td>

            {% if schedule_day.homework.name != "" %}
                <td rowspan="{{schedule_day.homework.numDays}}"><span class="schedule-homework">
                    <b>{{schedule_day.homework.name}}</b>
                    <br/>
                    {{schedule_day.homework.deadline}}
                    <br/>

                    {% if schedule_day.homework.link != "" %}
                    <a class="label label-red" href="{{schedule_day.homework.link}}">
                        <span class="material-symbols-outlined">description</span>Handout
                    </a>
                    {% endif %}
                </span></td>
                {% set ns.homework_days_left = schedule_day.homework.numDays - 1 %}
            {% else %}
                {% if ns.homework_days_left > 0 %}
                    {% set ns.homework_days_left = ns.homework_days_left - 1 %}
                {% else %}
                    <td><span class="schedule-homework"></span></td>
                {% endif %}
            {% endif %}
        </tr>
        {% endfor %}
    </tbody>

</table>

{% else %}
Coming Soon!
{% endif %}

</div>

