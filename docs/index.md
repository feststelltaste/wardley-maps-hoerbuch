---
layout: post
image: /images/header.png
---

![Eine Wardley Map, die die wichtigsten Ideen zu dieser Hörbuchversion des Buches von Simon Wardley charakterisiert.](images/header.png)

Dies ist eine synthetisch generierte Hörbuchversion von [Simon Wardleys](https://twitter.com/swardley) Buch ["Wardley Maps &ndash; Topographical intelligence in business"](https://medium.com/wardleymaps) in deutscher Sprache (eine [englische Version](https://feststelltaste.github.io/wardley-maps-audiobook/) gibt es auch).

_Derzeit handelt es sich um eine Vorab-Version mit ein [paar kleineren Fehlern](https://github.com/feststelltaste/wardley-maps-hoerbuch/issues). Das Hörbuch lässt sich aber dennoch gut anhören._

# Mitmachen!

Das generierte, deutschsprachige Hörbuch baut auf einer [maschinell übersetzten Version](https://github.com/selfscrum/wardley-maps-book/) auf. Wenn Dir Verbesserungen bei der Übersetzung einfallen, kannst Du diese gerne in dem [Übersetzungsprojekt](https://github.com/selfscrum/wardley-maps-book/issues) einbringen. Wenn Dir Dinge bzgl. der Aussprache auffallen, hinterlasse gerne einen [Hinweis für das Hörbuch](https://github.com/feststelltaste/wardley-maps-hoerbuch/issues). Die Übersetzung und das Hörbuch werden dann von Zeit zu Zeit aktualisiert.

# Downloads

Hier kannst Du das Hörbuch in verschiedenen Formaten herunterladen:

* [MP3-Format, mehrere Dateien gepackt als ZIP-Datei (413 MB)](https://www.feststelltaste.de/wp-content/uploads/share/Simon_Wardley_-_Wardley_Maps_Hoerbuch-mp3.zip)
* [OOG-Format, mehrere Dateien gepackt als TAR.GZ-Datei (214 MB)](https://www.feststelltaste.de/wp-content/uploads/share/Simon_Wardley_-_Wardley_Maps_Hoerbuch-ogg.tar.gz)

# Online-Version

Hier kannst Du die MP3s direkt auf der Website anhören. Sie sind in kleine Hörhäppchen für zwischendurch aufgeteilt. Viel Spaß!

{% for txt in site.static_files %}
{% if txt.path contains 'texts' and txt.path contains '.txt' %}
{% assign filename = txt.path | split: "/" | last | replace: ".txt", ".mp3" %}
{% assign title = txt.path | remove: "/texts/" | remove: ".txt" %}
<div>
<a href="{{ 'https://wardley-maps-hoerbuch.s3.eu-central-1.amazonaws.com/de-DE-Wavenet-B/mp3/' | append: filename | escape }}">{{title}}</a>

</div>
{% endif %}
{% endfor %}

# Mehr Informationen

- <http://list.wardleymaps.com> - Nützliche Ressourcen zum Thema Wardley Maps.
- <https://learnwardleymapping.com/> - Eine hervorragende Einführung in Wardley Maps.

{% include open-embed.html %}
