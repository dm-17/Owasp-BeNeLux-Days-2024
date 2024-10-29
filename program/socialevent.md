<div class="social-event">

<div align="center">
<!--
  <p>On Thursday evening we organize a social event in the local place "de Bierkantine", at a walking distance of around 10-15 minutes away from the conference venue.</p> -->
  <h1>Join us for the social event</h1>
  <br /><br />
  <p>When: 28/11/24 - 18:00</p>
  <p>Where: Ravellaan 96, Utrecht</p>
      <p ><a target="_blank" href="https://debierkantine.com"><img src="{{ site.baseurl }}/assets/images/BK-Zwart-Wit.png"></a></p>
  <p></p>
  <p><a target="_blank" href="https://graphhopper.com/maps/?point=52.08454%2C5.104077_Jaarbeurs%2C+Overste+den+Oudenlaan%2C+3527+KZ+Utrecht%2C+Utrecht%2C+Netherlands&point=52.083344%2C5.093331_De+Bierkantine%2C+Ravellaan+96%2C+3533JR+Utrecht%2C+Netherlands&profile=foot&layer=Omniscale">How to get there</a></p>


  <!-- <p>You are welcome to join us for a dinner and some drinks as of 18:00.</p><br /> -->
  <br /><br />
  <p>Dinner & Drinks are kindly offered by our sponsor:</p>
  

{% assign socialEventSponsors = site.data.sponsors | where:"level","Social event" | sort: 'name' %}

  {% if socialEventSponsors %}
    {% for sponsor in socialEventSponsors %}
      <div class="socialevensponsor">
        <a href="{{ sponsor.url }}" target="_blank"><img src="{{ site.baseurl }}/assets/images/sponsors/{{ sponsor.image }}" alt="{{ sponsor.name }} logo" style="{{ sponsor.style }}"/></a><br />
      </div>
    {% endfor %}
  {% endif %}
</div>
</div>
