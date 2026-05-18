---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
image:
    path: /assets/img/muttasaur-lilith-1.jpg
    alt: Lilith by Muttasaur
feeds:
    bsky: http://bsky.app/profile/did:plc:zcxjxvjfhujwf2nsoi4mc7aw/rss
gallery:
    - path: /assets/img/muttasaur-lilith-1.jpg
      alt: Beach Lilith by Muttasaur
    - path: /assets/img/muttasaur-lilith-2.jpg
      alt: DJ Lilith by Muttasaur
    - path: /assets/img/lilith-rave.jpg
      alt: Rave Lilith by NuTzy
    - path: /assets/img/lilith-collage.jpg
      alt: Goth Chic Lilith
    - path: /assets/img/lorart-lilith-1.jpg
      alt: Toothy Lilith by Lorart
    - path: /assets/img/lorart-lilith-2.jpg
      alt: Armed Lilith by Lorart
---

{% include fullsize-preview-image.html path=page.image.path alt=page.image.alt styles="object-position: top;" %}

## ∍⧽⧼∊ | ΘΔ | ♂♀
{: .text-center}

Hello there my pretty little pets~! I am Lilith, the "whatever the fuck I want to be" horned demon wolf. I do tech and cybersec by day, and horny furry shit by night. If you would like to find me, please use the socials links in the bottom left ♡♡
{: style="text-align: justify" }

I am a 20-something, queercoded, villanious therian, seeking Korps induction.

Conventions/Events I have been to:
- FurDU 2024
- MFC 2025
- Nocturnal 2025
- FurDU 2025
- Paws Outdoors Vibe Camp 2025
- MFC 2026
- Nocturnal 2026
- FurDU 2026

# Social Feeds
{: .text-center}

{% assign bsky_main = site.data.bsky_rss.rss.channel %}
{% capture name_link %}[{{ bsky_main.title | split: " - " | first }}]({{ bsky_main.link }}){% endcapture %}
### {{ name_link }}

> {{ bsky_main.description }}
{: .prompt-info}

#### Posts
{% assign bsky_rss = site.data.bsky_rss.rss.channel.item | sort: 'pubDate' | reverse %}
{% for item in bsky_rss limit: 6 %}
    {% assign item_desc = item.description %}
    {% assign pub_date = item.pubDate %}
    {% assign link = item.link %}
    {% capture attribution %}<br /><small><i>Posted on [{{ pub_date }}]({{ link }})</i></small>{% endcapture %}
> {{ item_desc | newline_to_br }} {{ attribution }}
{: .prompt-tip}

{% endfor %}

### .......
{: .text-center}

*See more at {{ name_link }}*
{: .text-center}

# Art Gallery
{: .text-center}

"You're on drugs!!" -> me, showing clear signs of being a wolf
{: .text-center}

{% include page-image-gallery.html image_gallery=page.gallery %}


#### ♡♡ thanks for visiting my website ♡♡
{: .text-center}