---
layout: delegation
---
{%- assign delegation=site.data.delegation-%}

{%- for info in delegation.info -%}
<div class="accordion">
  <a href="#" class="bp-accordion-header bp-accordion-button">
    <div class="speaker-img-wrapper">
      {%- if info.image-url -%}
      <div class="speaker-img">
        <img src="{{- site.baseurl -}}{{- info.image-url -}}" />
      </div>
      {%- endif -%}
      <h5>{{- info.name -}} {{- info.position -}}</h5>
      {%- if info.logo-url -%}
      <div class="org-logo">
        <img src="{{- site.baseurl -}}{{- info.logo-url -}}" />
      </div>
      {%- endif -%}
      <div class="icon-wrapper">
        <i class="sgds-icon sgds-icon-chevron-up"></i>
        <i class="sgds-icon sgds-icon-chevron-down"></i>
      </div>
    </div>
  </a>
  <div class="bp-accordion-body">
    <div class="speaker-content">
      <h6>Delegate's Bio:</h6>
      {{- info.description -}}
    </div>
  </div>
</div>
{%- endfor -%}
