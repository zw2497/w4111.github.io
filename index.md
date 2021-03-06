---
layout: index
---

#### Overview

The goal of this class is two-fold. First, to introduce you to core database concepts (e.g., data modeling, logical design, SQL) so that you too can build a billion dollar application. Second, to teach enough about database engine internals (e.g., physical database design, query optimization, transaction processing) so you have a good sense of why queries may be running slowly/incorrectly.

**Advanced Assignments**  There will several [optional extra-credit assignments](https://github.com/w4111/advanced) that will dive deeper into concepts introduced in class.   Some of them will involve extending a simple Python-based database engine with additional functionality!  They are labeled `AA#` in the schedule.  There is no obligation to do these, but they are available if you want to do then in addition to, or in lieu of the normal assignments.

<!--<center><span style="font-size: 20pt">Please do not ask me about the waitlist</span></center>-->

#### Announcements
* Update [AA2](https://github.com/w4111/advanced-public/blob/master/aa2.md) submit script.
* [Project 1 Part 3](https://github.com/w4111/project1-s19/blob/master/part3.md) released
* [Project 1 Part 2](https://github.com/w4111/project1-s19/blob/master/part2.md) released
* [AA2](https://github.com/w4111/advanced-public/blob/master/aa2.md) is out.
* HW 1.1 Solutions have been corrected. The deadline for HW1 Part 2 is now Friday midnight.
* HW1 results are out.
* Update on balancing releasing HW solutions with giving you time to turn assignments late.  We will wait 3 days and then reserve the right to release solutions anytime after that.  After solutions are released, we will stop accepting submissions.
* AA1 is out and can be found [here](https://github.com/w4111/advanced-public/blob/master/aa1.md). The databass to modify for AA1 can be found [here](https://github.com/w4111/databass-public/blob/master/README.md)
* HW0 results are out and can be found [here](https://github.com/w4111/hw0/blob/master/results.md).
* If you need to change your instabase username to your UNI, [fill out this form](https://docs.google.com/forms/d/e/1FAIpQLSdG1eY8_PoODroMax3TWk29h5IhWFkJYHYiZGX4BlYPrV209g/viewform) by end of class 1/29
* [Project 1 Part 1](https://github.com/w4111/project1) released
* [HW0](https://github.com/w4111/hw0) released.  Due Friday 1/25 10AM EST sharp.  Otherwise you will receive a 0 in the class.

#### Schedule

<table class="table table-striped schedule">
  <thead>
  <tr>
    <!--<th class="idx"></th>-->
    <th class="date" style="width: 5em; max-width: 5em;"> <p> <span>Date </span> </p> </th>
    <th style="min-width: 20%;"> <p> <span>Topic </span> </p> </th>
    <!--<th style="width: 15%"> <p> <span>Readings </span> </p> </th>-->
    <th style="width: 25%;"> <p> <span>Assigned</span> </p> </th>
    <th style="width: 25%;"> <p> <span>Due</span> </p> </th>
  </tr>
  </thead>
{% assign idx = 0 %}

{% for r in site.data.schedule %}
  {% assign idx = idx | plus: 1  %}
  <tr style="background-color: {{r.color}}; ">
    <!--<td class="idx">L{{idx}}</td>-->
    <td class="date">{{r.date}}</td>
    <td class="slug">
      {% if r.lshow == "1" %} <a href="{{r.link}}"> {% endif %}
        {{r.slug}}
      {% if r.lshow == "1" %} </a> {% endif %}
      {%if r.title %}: {{r.title}}{% endif %}
      {% if r.optional %}<br/>{{r.optional | safe}}{% endif%}
      
      {% if r.readings %}
        <br/>optional: Textbook {{r.readings | safe}}
      {% endif %}
      </td>
    <!--<td class="readings">{{r.readings | safe}}</td>-->
    <td>{% if 1 or r.ashow == "1" %} {{r.assigned | safe}} {% endif %}</td>
    <td>{% if 1 or r.dshow == "1" %} {{r.due | safe}} {% endif %}</td>
  </tr>
{% endfor %}
</table>


