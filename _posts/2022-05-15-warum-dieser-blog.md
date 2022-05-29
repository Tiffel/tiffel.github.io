---
layout: post
title:  "Warum dieser Blog"
---

### Warum überhaupt etwas online?
Gedanke 1: Ich möchte Familie und Freunden zeigen, was ich diesen Sommer so tue.

Gedanke 2: Ich möchte eine Art Tagebuch für mich selber führen. Es wird eine ganze Menge passieren und mich wird die Menge an Eindrücken vermutlich überwältigen. Deswegen ist der Plan, an jedem Ort zumindest einen Text zu den Eindrücken zu schreiben.

### Warum nicht Instagram, Twitter, $anyOtherSocialNetwork?
Ich hab nicht perse etwas gegen Meta, Twitter oder einen anderen Konzern. Ich tue das hier auch nicht aus Datenschutz Idealismuss. Dieser Blog läuft nichtmal auf eigener Infratruktur, sondern bei Github Pages.

Mein primärer Beweggrund ist, dass ich für mich selber eine Dokumentation haben möchte, die auch noch in 20 Jahren verfügbar ist. Und ob $Plattform dann noch existiert weiß einfach niemand.

Zusätzlich erwische ich mich bei der Nutzung von Sozialen Medien doch immer wieder, dass ich schaue, wer alles meinen Post sieht, liked etc. Das sorgt zwar auf der einen Seite für Glücksgefühle, macht aber auf der anderen Seite auch abhängig. Ich will das hier aber für mich selber tun und nicht in die Versuchung kommen, über Hashtags, gestellte Fotos und was auch immer mir Aufmerksamkeit zu holen.
Zusätzlich kann ich nicht auf der einen Seite über den Müllcontent auf Instagram meckern, auf der anderen Seite selber Content dort zuliefern.

Ein letzer Punkt aber sicherlich auch noch, dass ich Technik Bastelei mag. Die Challenge ist also hier nur von meinem Mobiltelefon mit Markdown Editor und einem Git Client den Content zu produzieren. Klar hätte ich mir auch ein Wordpress irgendwo hinlegen können, aber das wäre zu einfach. Nach den ersten Versuchen habe ich zwar gemerkt, dass das schon etwas masochistisch ist. Aber trotzdem habe ich es erfolgreich geschafft, ein Bild von gestern nachmittag hinzuzufügen. Der Durchstich ist also getan.

{% assign filenames = "PXL_20220514_162826611.MP.jpg" | split: "," %}
<div class ="image-gallery">
{% for name in filenames %}
    <div class="box">
    <a href="{{ site.imagesurl }}{{ name }}">
      <img src="{{ site.thumbsurl }}{{ name }} " alt="{{ name }}"  class="img-gallery" />
     </a>
    </div>
 {% endfor %}
</div>
