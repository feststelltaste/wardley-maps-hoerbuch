---
layout: post
image: /images/header.png
---


![Eine Wardley Map, die die wichtigsten Ideen zu dieser Hörbuchversion des Buches von Simon Wardley charakterisiert.](images/header.png)

Dies ist die (synthetisch erzeugte) Audioversion von [Simon Wardleys](https://twitter.com/swardley) Buch ["Wardley Maps &ndash; Topographical intelligence in business"](https://medium.com/wardleymaps).

**Die Übersetzung ist noch nicht gereviewt und das Hörbuch ist derzeit nur ein Entwurf!**

Nichtsdestotrotz kannst Du die MP3s hier anhören.

{% for txt in site.static_files %}
{% if txt.path contains 'texts' and txt.path contains '.txt' %}
{% assign filename = txt.path | split: "/" | last | replace: ".txt", ".mp3" %}
{% assign title = txt.path | remove: "/texts/" | remove: ".txt" %}
<div>
<a href="{{ 'https://wardley-maps-audiobook-de.s3.eu-central-1.amazonaws.com/hans/' | append: filename | escape }}">{{title}}</a>

</div>
{% endif %}
{% endfor %}

# Mehr Informationen

- <http://list.wardleymaps.com> - Nützliche Ressourcen zum Thema Wardley Maps.
- <https://learnwardleymapping.com/> - Eine hervorragende Einführung in Wardley Maps.

{% include open-embed.html %}
