---
# == NOTE ==
# Are you trying to edit the events?
#
# You will want to go to _data/events.yml. This page receives its data from there.

title: Events
---

{% assign events = site.data.events.events %}

{% if events.size > 0 %}
{%- for event in events -%}

## {{ event.name }}

**When**: {{ event.date }}, {{ event.start }} to {{ event.end }}

{{ event.description | escape }}

[{{ event.link_title }}]({{ event.link }})

{%- endfor -%}

{% else %}
There are no scheduled events.
{% endif %}