---
layout: default
permalink: /index.html
title: Insight Architectures
---

<p>Insight Architectures (IA) is a software architecture and development consultancy that delivers tailor-made software solutions and services to all kinds of businesses.</p>
<p>Founded in Stockholm in 2020, IA is a young company but one that is born out of 12+ years of experience in cloud-based software architecture and development, with a particular focus on .NET technologies, cloud-native backend architecture and AWS services. Combining this technical expertise with a strong focus on project design, Insight Architectures is able to plan and deliver business-ready software solutions that meet your organization’s needs and expectations, now and into the future.</p>

{% if jekyll.environment != 'production' %}
<div class="row expanded collapse">
  <div class="column">
    <div class="box-container">
      <div class="box">
        <span><i class="fas fa-database"></i></span>
        <h3>Architechture</h3>
        <p>Flank spare ribs capicola, strip steak biltong pancetta bresaola tri-tip cow landjaeger.</p>
        <div>
          <a href="#">Find out more</a> »
        </div>
      </div>
      <div class="box">
        <span><i class="fas fa-hands-helping"></i></span>
        <h3>Solutions</h3>
        <p>Strip steak biltong pancetta bresaola tri-tip cow landjaeger.</p>
        <div>
          <a href="#">Find out more</a> »
        </div>
      </div>
      <div class="box">
        <span><i class="fas fa-chart-line"></i></span>
        <h3>Future</h3>
        <p>Pork loin doner biltong shoulder meatball flank. Sirloin shankle ground round tail</p>
        <div>
          <a href="#">Find out more</a> »
        </div>
      </div>
    </div>
  </div>
</div>
{% endif %}

<h2 name="about-us">About us</h2>
<div class="row expanded collapse row-intro">
  <div class="small-12 column">
    <p>Insight Architectures (IA) is a software architecture and development consultancy with years of experience in delivering cloud-based software solutions to help organizations unlock business value. Combining strong technical expertise with an advanced project design approach, IA works together with clients to plan and execute business-ready software applications and architectures in line with business needs.</p>
    <p>At IA, we believe that a strong and consistently improved technological ecosystem is the basis for business success. That is why we pride ourselves in delivering software projects that are in line with the latest industry standards and designed to last into the future.</p>
    <p>IA was founded in Sweden in 2020 and currently has its headquarters in central Stockholm.</p>
  </div>
</div>

{% if jekyll.environment != 'production' %}
<h2 name="solutions">Our Solutions</h2>
<div class="row expanded collapse row-grid">
  <div class="medium-6 columns col-1">
    <div class="grid-content">
      <h3>Quality is seeking you</h3>
      <p>
        Pork loin doner biltong shoulder meatball flank. Sirloin shankle ground round tail, short loin
        prosciutto beef ribs salami pork pancetta kielbasa.
      </p>
    </div>
  </div>
  <div class="medium-6 columns col-2">
    <div class="grid-photo">
      <img src="/assets/images/photos/1.jpg" class="photo" />
    </div>
  </div>
</div>
<div class="row expanded collapse row-grid grid-reverse">
  <div class="medium-6 columns col-1">
    <div class="grid-content">
      <h3>Quality is seeking you</h3>
      <p>
        Pork loin doner biltong shoulder meatball flank. Sirloin shankle ground round tail, short loin
        prosciutto beef ribs salami pork pancetta kielbasa.
      </p>
    </div>
  </div>
  <div class="medium-6 columns col-2">
    <div class="grid-photo">
      <img src="/assets/images/photos/2.jpg" class="photo" />
    </div>
  </div>
</div>
{% endif %}

<h2 name="contact">Contact</h2>
<div class="row expanded collapse row-contact">
  <div class="small-12 medium-5 large-4 columns">
    <div class="contact-info">
      <h3>{{ site.data.company.name }}</h3>
      <div class="contact-org">
          <span>Org num:</span> <a href="https://www.allabolag.se/{{site.data.company.org-num | replace: '-', '' }}" target="_blank">{{ site.data.company.org-num }}</a><br>
          <span>VAT ID:</span> {{ site.data.company.vat-id }}
        </div>
      <br>
      <div class="contact-email">
        <i class="fas fa-envelope-square fa-fw"></i>
        <a href="mailto:{{ site.data.company.contacts.email }}">{{ site.data.company.contacts.email }}</a>
      </div>
      <div class="contact-phone">
        <i class="fas fa-mobile-alt fa-fw"></i>
        <a href="tel:{{ site.data.company.contacts.tel }}">{{ site.data.company.contacts.tel }}</a>
      </div>
      {% if jekyll.environment != 'production' %}
      <br/>
      <div class="contact-github">
          <i class="fab fa-github-square fa-fw"></i>
          <a href="{{ site.data.company.social.github.url }}">GitHub</a>
      </div>
      <div class="contact-linkedin">
          <i class="fab fa-linkedin fa-fw"></i>
          <a href="{{ site.data.company.social.linkedin.url }}">LinkedIn</a>
      </div>
      <div class="contact-twitter">
          <i class="fab fa-twitter-square fa-fw"></i>
          <a href="{{ site.data.company.social.twitter.url }}">Twitter</a>
      </div>
      {% endif %}
      <br>
      <h4>Visiting and mailing address</h4>
      <div class="contact-address">
          {{ site.data.company.contacts.visiting-address | newline_to_br }}
      </div>
    </div>
  </div>
  <div class="small-12 medium-7 large-8 columns">
    <div class="google-map">
      <iframe width="250" height="250" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0" src="https://maps.google.com/maps?width=250&amp;height=250&amp;hl=en&amp;q=Insight%20Architectures%20AB%20Kungsgatan%2060&amp;ie=UTF8&amp;t=&amp;z=14&amp;iwloc=B&amp;output=embed"></iframe>
    </div>
  </div>
</div>
