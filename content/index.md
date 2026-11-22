---js
const eleventyNavigation = {
	key: "About",
	order: 1
};
---
# About

Hullo, I'm Michael Sprague. I am interested in well, _everything_. To be more specific, machine learning, marketplaces, physics, quantum computing, and the writing of Vladimir Nabokov.

I have worked in consumer internet companies in machine learning/engineering (logistics, pricing, ranking, auctions), ML research in privacy/geospatial data, and quantum physics/computing (see more [Artifacts](/artifacts/)). Currently, I am a Director of Engineering at Yelp in Toronto, where I lead engineering for ads. Before Yelp, I managed machine learning teams at Deliveroo (now part of Doordash) in London. Before that, I did applied machine learning research at HERE Technologies, and I built the image-processing pipeline for an MRI-guided prostate cancer therapy at [Profound Medical](https://profoundmedical.com/), which is now an FDA-cleared medical device.

My first love was physics. I started out by ordering physics textbooks I didn't understand on Amazon. To resolve this, I studied [Engineering Physics](https://www.queensu.ca/physics/undergrad-studies/engineering-physics-program-overview/engineering-physics) at Queen's University for my undergraduate, [atomic physics/ultracold atoms](https://www.thywissenlab.ca/) from the University of Toronto for my master's, and finally a DPhil in [Atomic and Laser Physics](https://www.physics.ox.ac.uk/research/subdepartment/atomic-and-laser-physics) from Oxford, where I was a Clarendon Scholar researching quantum memories and entanglement. You can read [my DPhil thesis](/files/sprague-dphil-thesis.pdf) here.

You can reach me at michael.r.sprague@gmail.com
## [Blog](/blog/)

{% set postslist = collections.posts | head(-3) %}
{% set postslistCounter = collections.posts | length %}
{% include "postslist.njk" %}

{% if collections.posts | length > 3 %}
[See all posts →](/blog/)
{% endif %}
