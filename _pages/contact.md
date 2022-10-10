---
permalink: /contact-us/index.html
title: "Contact us"
hero: true
custom_style_sheet: contact
---

<div class="grid-x grid-margin-2">

  <div class="cell medium-4" style="padding-bottom: 20px;">
    <div style="padding-bottom: 20px;">
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
    </div>
    <div style="padding-bottom: 20px;">
      <h4>Visiting and mailing address</h4>
      <div class="contact-address">
          {{ site.data.company.contacts.visiting-address | newline_to_br }}
      </div>
    </div>
  </div>

  <div class="cell medium-8">
    <div class="google-map">
      <iframe width="250" height="250" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0" src="https://maps.google.com/maps?width=250&amp;height=250&amp;hl=en&amp;q=Insight%20Architectures%20AB%20Kungsgatan%2060&amp;ie=UTF8&amp;t=&amp;z=14&amp;iwloc=B&amp;output=embed"></iframe>
    </div>
  </div>
</div>
