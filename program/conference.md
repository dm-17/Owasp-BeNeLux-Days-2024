<div class="keynote-full">

{% if site.data.conference[0].title %}
	{% assign speakers = site.data.conference | sort: 'time' %}
	<h1>Conference day on 28/11/2024: Program Schedule</h1>
	<table>
	{% for speaker in speakers %}
		{% assign fullname="" %}
		{% if speaker.name2 %} 
			{% capture fullname %}{{speaker.name}} and {{speaker.name2}}{% endcapture %}
		{% else %}
			{% capture fullname %}{{speaker.name}}{% endcapture %}
		{% endif %}
		<tr>
			<td>{{speaker.time}}</td>
		{% if speaker.display %}
			<td>{{fullname}}</td>
			<td><a href="{{ site.baseurl }}/program/conference#{{fullname | replace: " ","-"}}">{{speaker.title}}</a></td>
		{% else %}
			<td colspan="2" align="center">{{speaker.title}}
			{% if speaker.name %}
				by {{fullname}}
			{% endif %}
			</td>
		{% endif %}
		<td>
		{% if speaker.feed %}
		<a href="{{speaker.feed}}"><img class="youtube" src="{{ site.baseurl }}/assets/images/conference/youtube_social_icon_red.png"></a>
		{% endif %}
		</td>
		</tr>
	{% endfor %}
	</table>

	<br><br>

	<h1>Confirmed speakers for Thursday 28/11/2024:</h1>
	<br />
	<ul>
	{% for speaker in speakers %}
		{% if speaker.display %}
			{% assign fullname="" %}
			{% if speaker.name2 %} 
				{% capture fullname %}{{speaker.name}} and {{speaker.name2}}{% endcapture %}
			{% else %}
				{% capture fullname %}{{speaker.name}}{% endcapture %}
			{% endif %}
		<li>
        <a name="{{fullname | replace: " ","-"}}">
        <img style="background-image: url({{ site.baseurl }}/assets/images/conference/{{speaker.image | default:'owasp_logo.png'}});{{speaker.style}};">
		{% if speaker.image2 %}
		<img style="background-image: url({{ site.baseurl }}/assets/images/conference/{{speaker.image2 | default:'owasp_logo.png'}});{{speaker.style}};; margin-top: 210px;">
		{% endif %}
		</a>
      {% if speaker.title %}
        <h2>{{speaker.title}} by {{fullname}}</h2>
      {% else %}
        <h2>{{fullname}}</h2>
      {% endif %}

      <p><em>{{speaker.time}}</em>
      {% if speaker.feed %}
          - <a href="{{ site.baseurl }}/program/feeds#{{fullname}}">Check out the streaming feed!</a>
      {% endif %}
      </p>

      {% if speaker.abstract %}
			<br>
        <h3>Abstract:</h3>
          <p>{{speaker.abstract}}</p>
          <br>
      {% endif %}
      {% if speaker.bio %}
        <h3>Bio:</h3>
	<p>{{speaker.bio}}</p>
        <br>
      {% endif %}
	  {% if speaker.linkedin or speaker.x_handle or speaker.infosec %}
        <h3>Follow {{fullname}}:</h3>
		{% if speaker.linkedin %}
			<a href="{{speaker.linkedin}}" title="{{speaker.name}}'s Linkedin page" target="_blank"><img class="socialnetworks" src="{{ site.baseurl }}/assets/images/conference/linkedin.png"></a>
		{% endif %}
		{% if speaker.linkedin2 %}
			<a href="{{speaker.linkedin2}}" title="{{speaker.name2}}'s Linkedin page" target="_blank"><img class="socialnetworks" src="{{ site.baseurl }}/assets/images/conference/linkedin.png"></a>
		{% endif %}
		{% if speaker.x_handle %}
			<a href="{{speaker.x_handle}}" title="{{speaker.name}}'s X handle" target="_blank"><img class="socialnetworks" src="{{ site.baseurl }}/assets/images/conference/x_handle.jpg"></a>
		{% endif %}
		{% if speaker.x_handle2 %}
			<a href="{{speaker.x_handle2}}" title="{{speaker.name2}}'s X handle" target="_blank"><img class="socialnetworks" src="{{ site.baseurl }}/assets/images/conference/x_handle.jpg"></a>
		{% endif %}
		{% if speaker.infosec %}
			<a href="{{speaker.infosec}}" title="{{speaker.name}}'s Infosec handle" target="_blank"><img class="socialnetworks" src="{{ site.baseurl }}/assets/images/conference/infosec.png"></a>
		{% endif %}
      {% endif %}
		</li>
		{% endif %}
		<br /><br />
	{% endfor %}
	</ul>
{% else %}
  <p><br>
     We're currently in the progress of making the conference program.<br>
     We will share the information very soon.
  </p>
{% endif %}
</div>
