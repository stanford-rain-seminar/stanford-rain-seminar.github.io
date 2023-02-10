---
layout: default
meta-description: "The RAIN (Research on Algorithms and Incentives in Networks) seminar provides a gathering place for talks and social discussion in this area.."
---

# Stanford RAIN (Research on Algorithms and Incentives in Networks) Seminar

The Internet is a complex network made of both machines and people, and hence, problems in this domain often require techniques from both algorithms and the social sciences. The RAIN (Research on Algorithms and Incentives in Networks) seminar, supported by [SOAL](https://web.stanford.edu/group/soal/), provides a gathering place for talks and social discussion in this area.


* Our talks this year are Wednesdays 12 PM PT in Y2E2 101!
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

**Seminar Organizers:** [Itai Ashlagi](http://www.stanford.edu/~iashlagi), [Grace Guan](https://guanzgrace.github.io/).

**Faculty Involved:** [Itai Ashlagi](https://web.stanford.edu/~iashlagi/), [Ashish Goel](https://web.stanford.edu/~ashishg/), [Ramesh Johari](http://www.stanford.edu/~rjohari/), [Amin Saberi](https://web.stanford.edu/~saberi/), [Aaron Sidford](https://web.stanford.edu/~sidford/), [Johan Ugander](https://web.stanford.edu/~jugander/), [Irene Lo](https://sites.google.com/view/irene-lo), [Ellen Vitercik](https://vitercik.github.io/)


**Note for Speakers:** The talk is 55 minutes including questions (as we often start a couple of minutes late). If you are giving a talk at RAIN, please plan a 45-50 minute talk since the audience usually ask a lot of questions. Also, the audience is fairly knowledgeable, so speakers should not feel obligated to provide basic game-theoretic, algorithmic, societal, industrial, probabilistic, or statistical background.


Website template from the [Stanford MLSys Seminar Series](https://mlsys.stanford.edu).

