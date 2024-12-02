<div class="social-event">

  <h1>Join us for the social event</h1>
  <p>We selected the following options for the social event menu:</p>

  <div class="socialEventBox">
    <h1>Menu</h1>
    <h2>Starters</h2>
    <ul>
    <li>BBQ Bites - Grill Mix</li>
    </ul>
    <br />
    <h2>Main</h2>
    <ul>
    <li>Option Meat: Classic Cheeseburger</li>
    <li>Option Vegan: VegaBurger (Beyond Meat)</li>
    </ul>
    <p class="note">Both options are served with french fries and salad</p>
    <h2>Dessert</h2>
    <ul>
    <li>Selection of the day</li>
    </ul>
    <div class="socialEventPrice">
      
        <button>
          <span id="price">15€</span>
          <br />
          <span id="detail">per person</span>
        </button>

    </div>
  </div>
  <div class="socialEventBox">
    <h1>When</h1>
    Thursday<br />
    28/11/24<br />
    19h00
  </div>
  <div class="socialEventBox">
    <h1>Where</h1>
        <a target="_blank" href="https://debierkantine.com"><img src="{{ site.baseurl }}/assets/images/BK-Zwart-Wit.png"></a>
    <br /><br />
    Ravellaan 96, Utrecht
    <br /><br />
    <div class="maplink">
      <a target="_blank" href="https://graphhopper.com/maps/?point=52.08454%2C5.104077_Jaarbeurs%2C+Overste+den+Oudenlaan%2C+3527+KZ+Utrecht%2C+Utrecht%2C+Netherlands&point=52.083344%2C5.093331_De+Bierkantine%2C+Ravellaan+96%2C+3533JR+Utrecht%2C+Netherlands&profile=foot&layer=Omniscale">Map and Itinerary</a>
    </div>
  </div>
  <div class="register">
    <button class="registerButton">Register now</button> 
  </div>

  <div class="sponsor">
    <p>Drinks are kindly offered by our sponsor:</p>
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
