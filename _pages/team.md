---
permalink: /team/index.html
title: Our team
custom_style_sheet: team
link_to_page: false
---

<div class="grid-container">
    <div class="grid-x grid-margin-x small-up-2 medium-up-4">
    {%- for member in site.data.team -%}
        <div class="cell">
            <div class="card">
                <img src="/assets/images/team/{{ member.id }}.jpg" alt="{{ member.first_name}} {{ member.last_name}}"/>
                <div class="card-section">
                    {% if page.link_to_page %}
                    <h4><a href="{{ member.id | datapage_url: '/team' }}">{{ member.first_name}} {{ member.last_name}}</a></h4>
                    {% else %}
                    <h4>{{ member.first_name}} {{ member.last_name}}</h4>
                    {% endif %}
                    {%- if member.role -%}
                    <p>{{ member.role }}</p>
                    {%- endif -%}
                    <div class="contacts fa-lg text-right">
                        {%- if member.resume -%}
                        <a href="{{member.resume}}" title="Download the resume" target="_blank"><i class="far fa-file"></i></a>
                        {%- endif -%}
                        {%- if member.calendly -%}
                        <a href="{{ member.calendly }}" title="Schedule a meeting" target="_blank"><i class="far fa-calendar-alt"></i></a>
                        {%- endif -%}
                        {%- if member.email -%}
                        <a href="mailto:{{ member.email }}" title="Send an email" target="_blank"><i class="fas fa-envelope"></i></a>
                        {%- endif -%}
                        {%- if member.linkedin -%}
                        <a href="{{ member.linkedin }}" title="Visit me on Linkedin" target="_blank"><i class="fab fa-linkedin"></i></a>
                        {%- endif -%}
                        {%- if member.github -%}
                        <a href="{{ member.github }}" title="Visit me on GitHub" target="_blank"><i class="fab fa-github"></i></a>
                        {%- endif -%}
                        {%- if member.twitter -%}
                        <a href="{{ member.twitter }}" title="Follow me on Twitter" target="_blank"><i class="fab fa-twitter"></i></a>
                        {%- endif -%}
                        {%- if member.homepage -%}
                        <a href="{{ member.homepage }}" title="Visit my homepage" target="_blank"><i class="fas fa-globe-europe"></i></a>
                        {%- endif -%}
                    </div>
                </div>
            </div>
        </div>
    {%- endfor -%}
    </div>
</div>
