---
title: "CMU 05-332/632: Assistive Technology and Accessibility"
hide:
  - navigation
---


# CMU 05-332/632: Assistive Technology and Accessibility


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

## Instructors and Logistics

**Canvas:** [https://canvas.cmu.edu/courses/47948](https://canvas.cmu.edu/courses/47948)  
**Semester:** Fall 2025  
**Instructors:** [Patrick Carrington](https://www.patrickcarrington.com) (Office Hours: [By Appointment](https://www.calendly.com/patrickcarrington/officehours), 407 S. Craig St. Room 201)  
**Co-Instructor:** [Franklin Mingzhe Li](https://www.franklin-li.com) (Office Hours: By Appointment, 407 S. Craig St. Room 212)        
**Meeting Time:** Monday / Wednesday 11:00 AM to 12:20 PM  
**Location:** GHC 4215  