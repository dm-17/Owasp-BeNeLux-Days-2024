---
title: Relive the conference
---

<div class="feeds-full">
	<table>
  <thead>
    <td>Speaker</td>
    <td>Title</td>
    <td>Time</td>
    <td>Feed</td>
    <td>Speaker link</td>
  </thead>
	{% assign speakers = site.data.conference | sort: 'time' %}
	{% for speaker in speakers %}
		{% if speaker.name %}
      {% if speaker.feed %}
        <tr>
	  <td>
		{% if speaker.name2 %} 
			{% capture fullname %}{{speaker.name}} and {{speaker.name2}}{% endcapture %}
		{% else %}
			{% capture fullname %}{{speaker.name}}{% endcapture %}
		{% endif %}
		{% if speaker.name and speaker.title and speaker.abstract %}
			<a href="{{ site.baseurl }}/program/conference#{{fullname | replace: " ","-"}}"><img class="thumbnail" src="{{site.baseurl}}/assets/images/conference/{{speaker.image | default:'owasp_logo.png'}}">
				{% if speaker.image2 %}
					<img class="thumbnail" src="{{site.baseurl}}/assets/images/conference/{{speaker.image2 | default:'owasp_logo.png'}}">
				{% endif %}
				{{fullname}}</a>
		{% endif %}
          </td>
        <td><a href="{{ site.baseurl }}/program/conference#{{fullname | replace: " ","-"}}">{{speaker.title}}</a></td>
        <td><em>{{speaker.time | replace: " ", ""}}</em></td>
        <td><a href="{{speaker.feed}}"><img class="youtube" src="{{ site.baseurl }}/assets/images/conference/youtube_social_icon_red.png"></a></td>
        <td>
        {% if speaker.url %}
          <a href="{{speaker.url}}">{{speaker.urltag}}</a>
        {% endif %}
        </td>
        </tr>
      {% endif %}
		{% endif %}
	{% endfor %}
	</table>
</div>
