---
layout: page
title: Dashboard || U.S. Open Data
---

# Project Dashboard

<link href="/css/dashboard.css" rel="stylesheet">

<div id="dashboard">

We have projects underway to help to build the capacity of open data. Here is the status of all of our projects.

{% for project in site.data.dashboard %}
  <div class="project">
    <div>
   		<h2>{{ project.title }} <span class="status {{ project.status }}">{{ project.status }}</span></h2>
    </div>
    <div>
	    <p>{{ project.description }}</p>
    </div>
   
	<div>
	    {% if project.contractor != null %}
	    <p>Contractor: <a href="{{ project.contractor_url }}">{{ project.contractor }}</a></p>
	    {% endif %}
	    
	    <ul>
	    {% if project.repository != null %}
	    <p><a href="{{ project.repository }}">Repository</a></p>
	    {% endif %}
	   
	    {% if project.blog_entry != null %}
	    <p><a href="{{ project.blog_entry }}">Blog Entry</a></p>
	    {% endif %}
	   
	    {% if project.website != null %}
	    <p><a href="{{ project.website }}">Website</a></p>
	    {% endif %}
	    </ul>
    </div>
    
  </div>
{% endfor %}

</div>
