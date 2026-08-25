---
layout: default
meta-description: "The RAIN (Research on Artificial Intelligence and Incentives) seminar is a hub for talks on the theory and practice of AI in strategic and societal settings."
---

# Stanford RAIN Seminar

Stanford RAIN (**R**esearch on **A**rtificial Intelligence and **IN**centives) is a seminar on the theory and practice of AI in strategic and societal settings. It serves as a hub for talks and discussion at the intersection of AI, incentives, and society. It is supported by Stanford’s Society & Algorithms Lab ([SOAL](https://web.stanford.edu/group/soal/)), [Stanford OpenLab](https://openlab.stanford.edu/), the [Stanford Center for Computational Market Design](https://marketdesign.stanford.edu/), and the [Stanford Computer Forum](https://forum.stanford.edu/) (and is open to Stanford Computer Forum affiliates).

* Autumn 2026 talks are held in person on Tuesdays from 4:30–5:30 PM PT; room assignments are listed below.
* [Join the RAIN mailing list]({{ site.mailing_list_url }}) to receive announcements and reminders.

{% for category in site.data.talks %}
<h2 id="{{ category.type | slugify }}">{{ category.type }}</h2>
{% include talk-list.html members=category.members %}
{% endfor %}

Browse the [RAIN seminar talk archive](/archive/).

{% include calendar.html %}

## About the Seminar

**Seminar Organizers:** [Amin Saberi](https://web.stanford.edu/~saberi/) and [Ellen Vitercik](https://vitercik.github.io/).

Website template from the [Stanford MLSys Seminar Series](https://mlsys.stanford.edu).
