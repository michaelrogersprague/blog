---
title: What I Talk About When I Talk About Testing
description: What I Talk About When I Talk About Testing.
date: 2026-11-23
---
>_"In long-distance running the only opponent you have to beat is yourself, the way you used to be."_  
 — Haruki Murakami, _What I Talk About When I Talk About Running_

At my first job, I was responsible for the image processing pipeline for a cancer treatment. We received raw phase and magnitude data from an MRI, and I converted the data to a real-time temperature measurement. The company was started in an academic lab and inherited some of its tools from that time, including MATLAB (I insist on full capitalization) for its data processing. We needed to re-implement all this proof-of-concept code in a proper programming language -- C# -- as part of the regulatory approval process. I knew little about C# -- "make no mistakes" pre-LLM. What I did have was an experimentally validated implementation in MATLAB as my test set. This was my key to learning C# safely -- I knew it was right when the differences between the two results were exactly zero. It also gave me more confidence in the MATLAB version because I could reimplement it in a different language, with different data structures and abstractions, and reach the same answer.

In the age of AI, this is hill climbing, those are evals. But it also gestures to an interesting question. Pre-AI, reimplementing the same logic in different languages, and even by different people, gave a margin of safety. The errors were uncorrelated (at least in part!<sup id="fnref-1"><a href="#fn-1">1</a></sup>), and the same answer increased the confidence of _both_ implementations. With AI, are the errors of the same LLM in different languages uncorrelated? What about different LLMs (Neon vs Opus vs Astra) -- are their errors uncorrelated?

Two recent studies have revisited N-version programming for AI, varying languages, models, and prompting strategies to measure how correlated the errors are.<sup id="fnref-2"><a href="#fn-2">2</a></sup> Using different models mattered more than using different languages or prompts with the same model. Combining versions did reduce errors, but mixed-model ensembles captured only about half of the reliability gain you would expect if the errors were uncorrelated, and single-model ensembles captured less than a third.

Does this mean that LLMs mirror some of the lack of independence observed in humans? Does this mean there are objectively hard parts of problems that confuse human and AI alike? Perhaps. But I do expect that adding diversity in AI thought -- adding uncorrelated error -- will be valuable for the future construction of Artificial Intelligence. So far, the lowest errors are from human + AI.<sup id="fnref-3"><a href="#fn-3">3</a></sup>

---

<ol class="footnotes">
<li id="fn-1">It's not quite true that the errors of multiple humans writing the same code are uncorrelated. A classic study by Knight and Leveson showed that N-version programming did <em>not</em> produce statistically independent errors; however, combining solutions from multiple people still reduced the error rate. J. C. Knight and N. G. Leveson, <a href="https://doi.org/10.1109/TSE.1986.6312924">An experimental evaluation of the assumption of independence in multiversion programming</a>, <em>IEEE Transactions on Software Engineering</em> 12(1), 96–109 (1986). <a href="#fnref-1" aria-label="Back to text">↩</a></li>
<li id="fn-2"><a href="https://arxiv.org/abs/2607.02808">A Systematic Methodology for Evaluating Failure Independence in LLM-Generated Code</a> (2026); and <a href="https://arxiv.org/abs/2606.20158">N-Version Programming with Coding Agents</a> (2026). <a href="#fnref-2" aria-label="Back to text">↩</a></li>
<li id="fn-3">Almeida et al., <a href="https://arxiv.org/abs/2607.03174">Effectiveness of LLM-based Software Diversity for Reliability Improvement – an Empirical Study</a> (2026). <a href="#fnref-3" aria-label="Back to text">↩</a></li>
</ol>
