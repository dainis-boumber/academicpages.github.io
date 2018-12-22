---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

Dainis Boumber, Yifan Zhang, Arjun Mukherjee, “Experiments with Convolutional Neural Networks for Multi-Label Authorship Attribution”, LREC 2018, 11th Conference on Language Resources and Evaluation.

Vilalta R., Dhar Gupta K., Boumber D., Meskhi M. M., “A General Approach to Domain Adaptation with Applications in Astronomy”, Publications of the Astronomical Society of the Pacific (PASP), 2018, IOP Science Press.

Pablo Guillen (University of Houston), German Larrazabal (Repsol USA), Gladys González (Repsol USA) Dainis Boumber (University of Houston), Ricardo Vilalta (University of Houston), “Supervised learning to detect salt body”, 2015 SEG’s International Exposition and 85th Annual Meeting in New Orleans, Louisiana.

W. Shi, Y. Wen, Z. Liu, X. Zhao, D. Boumber, R. Vilalta and L. Xu, “Scalable and Fault Resilient Physical Neural Networks on a Single Chip”, CASES 2014.

Tao Feng, Zhimin Gao, Dainis Boumber, Tzu-Hua Liu, Nicholas DeSalvo, Xi Zhao and Weidong Shi, “USR: Enabling Identity Awareness and Usable App Access Control During Hand-free Mobile Interactions.” Mobicase 2014.

Lee, Z. Liu, X. Tian, D. H. Woo, W. Shi, D. Boumber, Y. Yan, and K. Kwon, “Acceleration of bulk memory operations in a heterogeneous multicore architecture”, PACT 2012.

T. Feng, Z. Liu, B. Carbunar, D. Boumber and W. Shi, “Continuous Remote Mobile Identity Management Using Biometric Integrated Touch-Display”, MICRO Workshops 2012: 55-62.

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
