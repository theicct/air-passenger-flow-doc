---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: ICCT Passenger Flow Tensor Documentation
---

The ICCT Passenger Flow Tensor (T_ijk) is a calibrated 12×12×12 array of modelled annual air passenger flows at the granularity of the 12 RICE (Regional Integrated Climate–Economy) model regions. Each entry T[i, j, k] represents travellers originating in region i who transit through region j en route to destination k. The tensor is built as the missing calibration input for a Walrasian equilibrium model of aviation tax incidence developed at the Potsdam Institute for Climate Impact Research (PIK), in collaboration with the ICCT.

The T_ijk model synthesises two data sources — the ICCT segment-level emissions inventory and the Llano et al. (2023) bilateral tourism panel — via a two-stage multinomial logit routing model, and delivers a 2019-baseline tensor totalling 3.4 billion origin-destination passenger flows.

## Versions

The T_ijk model is under continuing development. Documentation of all versions is listed below.

{% assign pages = site.pages | sort: "sortable_version" | reverse %}
{% for page in pages %}
{% if page.dir contains '/versions/' and page.title contains 'T_ijk' %}
<li><a class="page-link" href="{{ page.url | relative_url }}">{{ page.title | escape }}</a></li>
{% endif %}
{% endfor %}
