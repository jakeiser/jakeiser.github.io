---
layout: page
header: true
title: Portfolio
permalink: /portfolio/
carousel:
- image: /assets/images/lphs-fine_tune_your_brain_2.jpg
- image: /assets/images/lphs-honour_concert.jpg
  border: true
- image: /assets/images/rusty_coleman_business_card.jpg
- image: /assets/images/arc_logo.png
- image: /assets/images/arc-wisse_festschrift_cover.png
- image: /assets/images/arc-cover.png
- image: /assets/images/cbtl_logo.png
- image: /assets/images/cbtl_bag.png
- image: /assets/images/collectors-universe-scottsdale_baseball_cards_logo.png
- image: /assets/images/biola-aa-poster-1.jpg

---

{% include carousel.html %}
---

<div style="position: fixed; width: 60%; margin: 240px auto 0 auto; padding: 30px">
<div class="flexslider">
<a class="nav-button previous" href="#"></a>
  <ul class="slides" style="text-align: center; margin: 0 20% 0 20%">
    {% for slides in page.carousel %}
    <li style="margin-bottom: 1em">
    {% if slides.link %}
    <a href="{{ slides.link }}"><img style="margin-top: 1em; border: 1px solid #a0a0a0; border-radius: 1.5%; box-shadow: 3px 3px 10px #a0a0a0" src="{{ slides.image }}"></a>
    {% else %}
    <img style="{% if slides.border %} border: 1px solid #a0a0a0 {% endif %}" src="{{ slides.image }}">
    {% endif %}
    </li>
   {% endfor %}
  </ul>
<a class="nav-button next" href="#"></a>
</div>

<!-- Counter
<span class="slide-current-slide"></span>
<span class="slide-total-slides"></span> -->

</div>

<!--/div-->

