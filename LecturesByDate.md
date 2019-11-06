---
layout: page
title: Slides
desc: "2019 Fall UVa CS 6316 Machine Learning Lectures Organized by Given Order"
---


<p><a name="topPage"></a></p>

<div class="posts">

----  ----  
{% assign sorted = site.contents   %}
{% for post in sorted %}

  <div class="post">
    <h1 class="post-title">
      <a href="{{ site.baseurl }}{{ post.url }}">
        {{ post.title }}
      </a>
    </h1>
 
 <ul>
  {% if post.lecture %}
  <li><a href="{{ site.baseurl }}/Lectures/{{ post.lecture }}.pdf">Lecture: 
  {{ post.lecture }}</a></li>
  <li>Version: {{ post.lectureVersion }}</li>
  {% endif %}

  {% if post.extraContent %}
  <li>More to Read: <a href="{{ site.baseurl }}/Lectures/{{ post.extraContent }}.pdf">   {{ post.extraContent }} </a></li>
  {% endif %}

  {% if post.notes %}
  <li>Useful to Read: {{ post.notes }} </li>
  {% endif %}

  {% if post.video %}
  <li>Video: {{ post.video }} </li>
  {% endif %}

</ul>

  {% for temp in post.tags %}
    <a class="button" href="{{ site.baseurl }}/LecturesByTags/#{{temp | replace:" ","-" }}">{{ temp }}</a>
  {% endfor %}

<br>


  {% if post.lecture  %}
    {% if post.lectureVersion contains 'current' %}
<embed src="https://drive.google.com/viewerng/viewer?embedded=true&url=https://qiyanjun.github.io/2019f-UVA-CS6316-MachineLearning//Lectures/{{ post.lecture }}.pdf" width="800" height="595"> 
    {% endif %}
  {% endif %}


    {{ post.content }}


  </div>
<hr>

{% endfor %}
</div>


<div style="position: fixed; bottom: 76px; right:10px; width: 88px; height: 36px; background-color: #FFCF79;">
<a style="position: fixed; bottom:80px; right:10px;" href="#topPage" title="Back to Top">BackTop</a>
</div>


<hr>
