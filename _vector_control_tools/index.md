---
title: Vector Control Tools
permalink: /usefultools/
---

<div class="wrap-outer">
  <h1>Tools for vector control</h1>
  <p>
    There are many tools available that support the vector control community. Here are a few that you may be interested in.
  </p>

<div class="gallery">
{% for tool in site.data.vector_control_tools %}
  <a class="gallery-item" href="{{ tool.url }}">
    {% if tool.image %}
      <div class="gallery-item-image">
        <img src="{{ site.baseURL}}/assets/images/external_tools/{{ tool.image }}" alt="Example image of tool: {{tool.name}}">
      </div>
    {% endif %}
      <div class="gallery-item-body">
        <h2>{{ tool.name }}</h2>
        <p>
          <em><strong>Developed by:</strong> {{ tool.developer }}</em><br />
          <em><strong>Contact:</strong> {{ tool.contact_email }}</em>
        </p>
        <div>{{ tool.description }}</div>
        {% if tool.papers.size > 0 %}
          <div>
            <p style="margin-bottom:0;">Referenced in:</p>
            <ul>
              {% for paper in tool.papers %}
                <li>paper</li>
              {% endfor %}
            </ul>
          </div>
        {% endif %}
      </div>
  </a>
{% endfor %}
</div>

<div style="margin-top:3em;">
  <p>
    Have something you'd like to see here? <a href="submit">Submit your tool</a>.
  </p>
</div>

<div style="margin-top:3em;">
  <p style="font-size:smaller;">
    <em>
      Note: The tools presented here are developed by third parties for informational purposes only. The presence of a tool on this list is not intended to indicate endorsement or support by VectorSurv. VectorSurv does not guarantee the accuracy, reliability, availability, or security of these tools. We are not responsible for any content or functionality of third-party tools, and are not responsible for errors or damages arising from their use.
    </em>
  </p>
</div>
