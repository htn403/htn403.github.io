---
layout: default-container
---

<div class="row mb-3">
  <div class="col-md-3">
    <img src="/assets/homepage/profile.png" class="rounded float-left img-fluid" style="border: #ddd solid 1px" />
  </div>
  <div class="col-md">
    <p>
        <b>MSc, PhD</b> <br/>
        Postdoctoral Researcher <br />
        Current affiliation: School of Engineering,
        Brown University <br/>
184 Hope St, Providence, RI 02912 <br/>
        <b>Email</b>: <a href="mailto:nguyen.thaihoang@gmail.com">nguyen.thaihoang@gmail.com</a><br/>
        <span style="line-height:1.3em; font-size: 1.3em">
        <a href="https://github.com/minhptx"><i class="fab fa-github"></i></a>
        <a href="https://www.linkedin.com/in/minh-pham-b1405/"><i class="fab fa-linkedin"></i></a>
        <a href="https://www.researchgate.net/profile/Minh-Pham-16"><i class="fab fa-researchgate"></i></a>
        </span>
    </p>
  </div>
</div>

### Biography

I am a Ph.D. Candidate in the Computer Science Department at University of Southern California (USC) in Los Angeles. I am working as a research assistant at the [Center on Knowledge Graphs](http://usc-isi-i2.github.io/home/), advised by Prof. [Craig Knoblock](http://usc-isi-i2.github.io/knoblock/). Before joining USC in 2015, I earned my B.E. in Computer Science from [HCMC University of Technology](http://www.cse.hcmut.edu.vn/site/en/) (honor program) in 2014.

My research focuses on machine learning and AI techniques to reduce human effort in data integration. Particularly, I have been working on unsupervised and semi-supervised approaches for error detection and fact verification for tabular data. More information is available on my [resume](/assets/homepage/resume.pdf).


### Projects

<style>
#project-lst > div {
    padding-top: 10px;
    border: none;
    border-top: 1px solid rgba(0,0,0,.125);
}
#project-lst > div:first-child {
    border-top: none !important;
}
</style>

<div id="project-lst">
{% for project in site.data.projects %}
<div class="card mb-3">
  <div class="row no-gutters">
    <div class="col-sm-4 align-self-center">
        {% if project.image %}
        <img src="{{ project.image }}" class="card-img">
        {% else %}
        <!-- <svg class="bd-placeholder-img" width="100%" height="100" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid slice" focusable="false" role="img" aria-label="Placeholder: Image"><title>Placeholder</title><rect width="100%" height="100%" fill="#868e96"></rect><text x="50%" y="50%" fill="#dee2e6" dx="-2em" dy=".3em">No Image</text></svg> -->
        {% endif %}
    </div>
    <div class="col-sm-8">
      <div class="card-body">
        <h5 class="card-title">{{ project.name }}</h5>
        <p class="card-text">
        {% if project.descriptions %}
            <ul>
            {% for line in project.descriptions %}
            <li>{{ line }}</li>
            {% endfor %}
            </ul>
        {% else %}
        {{ project.description }}
        {% endif %}
        </p>
        <!-- <small class="card-text"><small class="text-muted">Last updated 3 mins ago</small></p> -->
        {% for link in project.links %}
        <a href="{{ link.url }} " class="btn btn-outline-primary">{{ link.name }}</a>
        {% endfor %}
      </div>
    </div>
  </div>
</div>
{% endfor %}
</div>

### Selected Publications

{% for paper in site.data.publications %}
- <a id="{{ paper.id }}" name="{{ paper.id }}"></a>[**{{ paper.title }}**]({{ paper.url }})<br/>
{{ paper.authors_pre }}**Minh Pham**{{ paper.authors_pos }}<br/>
{{ paper.published_in }}
{% endfor %}

### Awards

- **ISI Graduate Symposium**<br/>
Best Paper Award, 2019
- **Vietnam Education Foundation (VEF) Fellowship**<br/>
Fellow, 2015
- **HCMC University of Technology**<br/>
Outstanding Honor Student Award, 2010 - 2014
- Wood chop flow
