---
layout: default
meta-description: "The RAIN (Research on Artificial Intelligence and Incentives) seminar is a hub for talks on the theory and practice of AI in strategic and societal settings."
---

# Stanford RAIN (**R**esearch on **A**rtificial Intelligence and **IN**centives) Seminar

RAIN is a seminar on the theory and practice of AI in strategic and societal settings. Supported by Stanford’s Society & Algorithms Lab ([SOAL](https://web.stanford.edu/group/soal/)), it serves as a hub for talks and discussion at the intersection of AI, incentives, and society.


* Our talks are on Tuesdays from 4:30-5:30 PM PT (except 12/2, when its 4:00-5:00 PM) in Spilker 232!
* To receive updates on upcoming talks, please join our [email list](https://mailman.stanford.edu/mailman/listinfo/internetalgs)! 

{% for category in site.data.talks %}
# {{ category.type }}
<div class="talk-list">
  {% for talk in category.members %}
  <div class="talk list-group-item">
  <div class="talk-date">{{ talk.date }}</div>
  <div class="talk-presenter">{{ talk.speaker }}</div>
  {% if talk.title %}
  <div>
    {% if talk.recording %}
      <span><a class="talk-title-link" href="{{ talk.recording }}">{{ talk.title }} <i class="bi bi-box-arrow-up-right"></i></a></span>
    {% elsif talk.livestream %}
      <span><a class="talk-title-link" href="{{ talk.livestream }}">{{ talk.title }} <i class="bi bi-box-arrow-up-right"></i></a></span>
    {% else %}
      <span>{{ talk.title }}</span>
    {% endif %}
  </div>
  {% endif %}
  {% if talk.abstract %}
    <details>
    <summary>→ Abstract and Bio</summary>
    {{ talk.abstract }}
    
    {% if talk.bio %}
    <br><br>
    <strong>Bio: </strong> {{ talk.bio }}
    {% endif %}

    {% if talk.recording %}
      <br><br>
      <strong><a href="{{ talk.recording }}">Video Link</a></strong>
    {% elsif talk.livestream %}
      <br><br>
      <strong><a href="{{ talk.livestream }}">Livestream Link</a></strong>
    {% endif %}
    </details>
  {% endif %}
  </div>
  {% endfor %}
</div>
{% endfor %}

Previous talks can be found [here](/archive).

# About The Seminar

**Seminar Organizers:** [Amin Saberi](https://web.stanford.edu/~saberi/), [Nikil Selvam](https://www.nikilrs.com/), [Xizhi Tan](https://xizhitan.github.io/), [Ellen Vitercik](https://vitercik.github.io/).

**Faculty Involved:** [Itai Ashlagi](https://web.stanford.edu/~iashlagi/), [Ashish Goel](https://web.stanford.edu/~ashishg/), [Ramesh Johari](http://www.stanford.edu/~rjohari/), [Amin Saberi](https://web.stanford.edu/~saberi/), [Aaron Sidford](https://web.stanford.edu/~sidford/), [Johan Ugander](https://web.stanford.edu/~jugander/), [Irene Lo](https://sites.google.com/view/irene-lo), [Ellen Vitercik](https://vitercik.github.io/).


**Note for Speakers:** The talk is 55 minutes including questions (as we often start a couple of minutes late). If you are giving a talk at RAIN, please plan a 45-50 minute talk since the audience usually ask a lot of questions. Also, the audience is fairly knowledgeable, so speakers should not feel obligated to provide basic game-theoretic, algorithmic, societal, industrial, probabilistic, or statistical background.


Website template from the [Stanford MLSys Seminar Series](https://mlsys.stanford.edu).
