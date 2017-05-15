---
title: Exam Dates
year: inf1
ordering: -10
links:
  - name: search
    url: http://www.scripts.sasg.ed.ac.uk/registry/examinations/index.cfm
  - name: inf1-op allocations
    url: http://private.inf1.hgs.club/INF1-OP%20Exam%20-%2012th%20May%202017.pdf

exams:

  - name: CG
    location: Playfair Library
    date: Mon, 15th, 14:30-16:30 (2hrs)
    time: 1494858600
    code: INFR08020
    optional: true

  - name: DA
    location: Pleasance Sports Hall
    date: Tues, 16th, 09:30-11:30 (2hrs)
    time: 1494927000
    code: INFR08015

---


<small>It's only first year. **You only need 40% and it doesn't contribute to your final grade.** Chill, it's no big deal.</small>

<table style="width: 100%;">
    <tr>
        <th>Exam</th>
        <th>Location</th>
        <th>Date</th>
        <th></th>
        <th></th>
    </tr>


    {% for exam in page.exams %}
    <tr {% if exam.optional %}class="hoverRow"{% endif %}>
      <td>{{ exam.name }}</td>
      <td>{{ exam.location }}</td>
      <td>{{ exam.date }}</td>
      <td class="examTime" data-time="{{ exam.time }}"></td>
      <td><button onclick="searchExam('{{ exam.code }}')">View</button></td>
    </tr>
    {% endfor %}
</table>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.16.0/moment.min.js"></script>
<script src="/static/js/exam-script.js"></script>