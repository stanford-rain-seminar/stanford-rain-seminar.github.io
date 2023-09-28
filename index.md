---
layout: default
meta-description: "The RAIN (Research on Algorithms and Incentives in Networks) seminar provides a gathering place for talks and social discussion in this area.."
---

# Stanford RAIN (Research on Algorithms and Incentives in Networks) Seminar

The Internet is a complex network made of both machines and people, and hence, problems in this domain often require techniques from both algorithms and the social sciences. The RAIN (Research on Algorithms and Incentives in Networks) seminar, supported by [SOAL](https://web.stanford.edu/group/soal/), provides a gathering place for talks and social discussion in this area.


* Our talks for the Autumn 2023 quarter are on Mondays 4 PM PT in Y2E2 299!
  (Except for the first talk on 9/29, which is at 2pm in Y2E2 101)
* To receive updates on upcoming talks, please join our [email list](https://mailman.stanford.edu/mailman/listinfo/internetalgs)!

<div class="talk-list">
  <div class="talk list-group-item">
  <div class="talk-date">{{ Sept. 29, 2023 }}</div>
  <div class="talk-presenter">{{ Elaine Shi }}</div>
  <div>
      <span>{{ Decentralized Mechanism Design }}</span>
  </div>
    <details>
    <summary>→ Abstract and Bio</summary>
    {{ In transaction fee mechanism design, users bid to get their transactions confirmed in the block. Classical auctions completely fail in such a decentralized environment where even the auctioneer (i.e., miners) can be a strategic player. Further, the miners can collude with a subset of the users, e.g., facilitated by real-world platforms like Flashbots. A line of works have attempted to devise a 'dream' transaction fee mechanism but all have failed. In this talk, I will first show that this is not a coincidence --- in fact, there is a fundamental mathematical barrier towards achieving a 'dream' transaction fee mechanism. Then, I will explain how to overcome impossibilities with the help of cryptography, leading to practical mechanisms that achieve good social welfare and revenue. }}
    <br><br>
    <strong>Bio: </strong> {{ Elaine Shi is an Associate Professor at Carnegie Mellon University. Prior to joining CMU, she taught at Cornell and the University of Maryland. Her research interests include cryptography, security, algorithms, mechanism design, and foundations of blockchains. She has won numerous awards such as the Sloan Fellowship, the Packard Fellowship, the ONR YIP award, the NSA Best Science of Cybersecurity Paper award, Cylab Distinguished Alumni Award, and various other best paper awards. Her work on Oblivious RAM and privacy-preserving algorithms have been deployed at a large scale by companies like Signal, Google, and JP Morgan. }}
  </div>
</div>

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

**Seminar Organizers:** [Itai Ashlagi](http://www.stanford.edu/~iashlagi), [Mohak Goyal](https://sites.google.com/view/mohakg/home), [Tristan Pollner](https://tristanpollner.com).

**Faculty Involved:** [Itai Ashlagi](https://web.stanford.edu/~iashlagi/), [Ashish Goel](https://web.stanford.edu/~ashishg/), [Ramesh Johari](http://www.stanford.edu/~rjohari/), [Amin Saberi](https://web.stanford.edu/~saberi/), [Aaron Sidford](https://web.stanford.edu/~sidford/), [Johan Ugander](https://web.stanford.edu/~jugander/), [Irene Lo](https://sites.google.com/view/irene-lo), [Ellen Vitercik](https://vitercik.github.io/).


**Note for Speakers:** The talk is 55 minutes including questions (as we often start a couple of minutes late). If you are giving a talk at RAIN, please plan a 45-50 minute talk since the audience usually ask a lot of questions. Also, the audience is fairly knowledgeable, so speakers should not feel obligated to provide basic game-theoretic, algorithmic, societal, industrial, probabilistic, or statistical background.


Website template from the [Stanford MLSys Seminar Series](https://mlsys.stanford.edu).

