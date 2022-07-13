---
permalink: /customers/index.html
title: Our customers
---

<div class="grid-container">
    <div class="grid-x grid-margin-x small-up-1 medium-up-1">
    {% assign customers = site.data.customers | sort_natural %}
    {% for customer in customers %}
        <a href="{{ customer.id | datapage_url: '/customers' }}">
        <div class="cell">
            <div class="card">
                <div class="card-section">
                    <h4>{{ customer.name}}</h4>
                    {%- if customer.short_description -%}
                    <p>{{ customer.short_description }}</p>
                    {%- endif -%}
                </div>
            </div>
        </div>
        </a>
    {%- endfor -%}
    </div>
</div>
