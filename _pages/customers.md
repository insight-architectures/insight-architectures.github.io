---
permalink: /customers/index.html
title: Our customers
custom_style_sheet: customers
---

<div class="grid-container">
    <div class="grid-x grid-margin-x small-up-1 medium-up-1">
    {% assign customers = site.customers | sort_natural: "title" %}
    {% for customer in customers %}
        <a href="{{ customer.url }}">
        <div class="cell">
            <div class="card">
                <div class="card-section">
                    <h4>{{ customer.title}}</h4>
                    {%- if customer.short_description -%}
                    <p>{{ customer.short_description }}</p>
                    {%- endif -%}
                </div>
                {%- if customer.tags.size > 0 -%}
                <div class="card-section">
                {% assign tags = customer.tags | sort_natural %}
                {%- for tag in tags -%}
                    <span class="tag">{{tag}}</span>
                {%- endfor -%}
                </div>
                {%- endif -%}
            </div>
        </div>
        </a>
    {%- endfor -%}
    </div>
</div>
