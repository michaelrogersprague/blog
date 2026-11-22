---js
const eleventyNavigation = {
	key: "About",
	order: 1
};
---
# About

Hullo, I'm Michael Sprague. I am interested in well, _everything_. To be more specific, machine learning, consumer marketplaces, physics, quantum computing, and the writing of Vladimir Nabokov -- see [Artifacts](/artifacts/) for papers, patents. 

Currently, I am a Director of Engineering at Yelp in Toronto, where I lead engineering for ads. Before Yelp, I managed machine learning teams at Deliveroo (now part of Doordash) in London. And before that, I did applied machine learning research at [HERE Technologies](https://www.here.com/), and I built the image-processing pipeline for an MRI-guided prostate cancer therapy at [Profound Medical](https://profoundmedical.com/).

My first love was physics. I started out by ordering physics textbooks I didn't understand on Amazon. I tried to rectify this by studying [Engineering Physics](https://www.queensu.ca/physics/undergrad-studies/engineering-physics-program-overview/engineering-physics) at Queen's University for my undergraduate, [atomic physics/ultracold atoms](https://www.thywissenlab.ca/) from the University of Toronto for my Master's, and finally a DPhil in [Atomic and Laser Physics](https://www.physics.ox.ac.uk/research/subdepartment/atomic-and-laser-physics) from Oxford, where I was a [Clarendon Scholar](https://www.ox.ac.uk/admissions/graduate/fees-and-funding/funding/clarendon) researching quantum memories and entanglement -- see [my DPhil thesis](/files/sprague-dphil-thesis.pdf) here.

You can reach me at michael.r.sprague@gmail.com
## [Blog](/blog/)

{% set postslist = collections.posts | head(-3) %}
{% set postslistCounter = collections.posts | length %}
{% include "postslist.njk" %}

{% if collections.posts | length > 3 %}
[See all posts →](/blog/)
{% endif %}
