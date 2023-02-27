---
title: 'The End of Academic NLP Research? Responsible Large Language Models and the Future of NLP at the 2023 HLPT Winterschool'
date: 2023-02-27
permalink: /posts/2023/02/winterschool-responsible/
image: https://raw.githubusercontent.com/myrthereuver/myrthereuver.github.io/master/_posts/2EE2B5C7-B6E2-48C2-B0F3-B12A3F893A2B.JPG
comments: true
tags:
  - PhD
  - Science
  - NLP
  - winter school
  - Learning
---
*This blog post describes my experiences at the Nordic HPLT Winter school - with also the very exciting panel “Is the End of Academic NLP Research in Sight?”*

<img src="https://raw.githubusercontent.com/myrthereuver/myrthereuver.github.io/master/_posts/2EE2B5C7-B6E2-48C2-B0F3-B12A3F893A2B.JPG" alt="picture of sunset at the conference hotel in the snow" style="width:400px;"/>

<sup>[Image: Myrthe Reuver, Sunset at the Conference Hotel)</sup>


From 6 to 8 February 2023, I was lucky enough to participate in the [2023 HPLT winter school on Large-Scale Language Modeling](http://wiki.nlpl.eu/index.php/Community/training) in Norway! This was a very exciting experience: I am now finally seeing academic debate in person - and not only through Twitter threads or online panels! I was known to livetweet these during the 2020 lockdowns, e.g. [a panel on ethics in NLP](https://twitter.com/myrthereuver/status/1328718156785995778) or one on [the effects of leaderboards on NLP research](https://twitter.com/myrthereuver/status/1329546565296459776). If you would like to read more about my experiences early in the PhD, you can read [my first blog post](https://myrthereuver.github.io/posts/2021/09/first-blog/) about this topic.


This in-person winterschool focussed on Large Language Models (LLMs), specifically multi-lingual, efficient, and responsible use of them and of very large, web-based datasets. The school also extensively discussed the role of NLP research in academia and in Big Tech, which I really liked as a fan of meta-scientific discussions!

Below, you can find a review of my personal highlights of this event. Other participants may have had different experiences or highlights! In terms of organization, the winterschool was a near-flawless experience. We were picked up by a bus at the airport in Oslo, and 3 hours later we arrived at the near-empty ski resort hotel surrounded by beautiful snowy scenery. The time given for outdoor exploration was very nice for connecting with researchers from different labs: I had some very useful talks with fellow PhDs on research and especially our career plans and ideas, as I feel the pressure now of the end of my PhD being closer than the start.. 😱

If you like (some of) the topics and highlights that I covered here, we may have shared research interests! Please reach out to me, either through email, Mastodon, or Twitter (see the sidebar on my website) if you have opportunities or ideas you want to share.

I summarized my experience in four broad themes: (1) Responsible Scraping & Documenting of Datasets, (2) the Panel on the Future of NLP,  (3) Responsible LLMs, and (4) Efficient LLMs.


# 1. Responsible Scraping & Documenting Datasets

Throughout the week, there were several talks on the datasets for LLMs. This was the first time I heard about the specific decisions and ideas behind large data scraping projects, so it was very useful to learn about this - it is, after all, what LLMs are pre-trained on!

One talk was on **Common Crawl** (presented by **[Sebastian Nagel](https://commoncrawl.org/about/team/#headshot-14714))** and another on **OSCAR** (presented by **[Pedro Ortiz Suarez](https://portizs.eu/)**). 

Both projects highlighted that the goal was not to scrape the entire web (which would be near-impossible) but to prioritize some URLs in a sample. There was some discussion on what a “representative” sample meant: the **Common Crawl** project went with top N URLS found with a metric called “harmonic centrality”, meaning URLs that had more URLs linked are prioritized, batch-wise. Their crawlers also respect robots.txt and do not crawl without permission: the dataset has less to almost no social media content due to robots.txt. The over-representation of English was also discussed: multilingual sites often prioritize English. Also, the crawler is based in Virginia and non-US sites are slower and have as default English due to localization and personalization. 

**OSCAR** started its life as a Digital Humanities project, and is since its conception trying to be multilingual, open and transparent, and high-quality. On this last point, there were several rule-based solutions to avoid low quality data: avoiding a high percentage of punctuation, avoiding SEO-hacked websites (and how useful it is to have an SEO expert in the project, to reverse-engineer the hacking!), and a blocklist of “adult”/porn content - which in practice led to the blocking of LGBTQ-related content and thus biases, which the project is now aware of and actively tries to correct. They also aim for representation, and in the new CaBerNET project they work on a French dataset with Biber’s definition of representation: capturing the full range of variability of language and text in the population. As a self-described definitions enthusiast, I really liked this! There also is an initiative now to have LLMs in every language, and OSCAR is developing a project to do so. 

The talk also had the great quote **“duplication is the great evil, and the only greater evil is SEO.”** ✨ I also enjoyed a short reflection on tokenizers, and metric of fertility: the number of tokens per byte, and lower is better (better to compute and more understandable). 


# 2. Panel on the Future of NLP

The first day ended with a panel discussion on the future of NLP in academia, with the intense title “Is the End of Academic NLP Research in Sight?”, and discussed three scenarios for the situation of NLP research in 2050.  The participants were [Ivan Vulić](https://sites.google.com/site/ivanvulic/), [Emily M. Bender](https://faculty.washington.edu/ebender/), and [Oskar Holmström](https://liu.se/en/employee/oskho10), and they each presented a different future vision of NLP in universities. 

The first scenario was called **“back to the ivory tower”** 🌇, and highlighted how one direction could be to go back to research uninteresting for large companies. Ivan really presented this direction with much flair, quoting Pink Floyd songs that did not fully make it to my notes. He highlighted that this is an unlikely scenario, and the discussion in the panel then went to this scenario allowing universities to be able to pick their own battles and “exploration rather than exploitation”.  

The second scenario was presented by Emily and had the title **“NLP as a social science”** 📊. The key development here is that the focus goes (back?) to interdisciplinary work and the effects of NLP and also studying language use in society. This scenario has national funding separate from company and technology related research funding. The panelists and also the audience discussed that for this future scenario, a positive feedback loop is needed from one of the powers academics have in shaping research agendas: through reviews. If reviewers are positive about this research direction, this research direction becomes more established, prestigious, and funded. 

The third scenario was presented by Oskar, and was called **“the Return of the Jedi”**💥. The main idea presented in this scenario was that NLP needs to compete with the large-scale, huge language modelling-based approach from different industry labs. Different universities work together in hubs and large, national computing clusters, and there is a large computing center that is like the CERN of AI and jointly owned by all universities in the world. There was general enthusiasm in the audience about this scenario, also part due to the vivid Yoda imagery.

All winter school participants in the end voted for a scenario, with most preferring this third scenario. I realized that I would really like the second scenario, but as half a computational social scientist this may be somewhat biased. 😉 


# 3. Responsible LLMs

Another theme in this winter school focussed on responsible LLMs, both in training and applications.

One talk falling into this category was by **[Mehdi Ali](https://github.com/mali-git)** on **OpenGPT-X**: a version of GPT but trained by publicly funded researchers, and inside Europe. Special mention was on an increase of factual correctness of this model, having actually quality data and no contaminated data (e.g. test or validation data in the pre-training phase), and adapting to new languages. Their main idea is a “knowledge-driven LLM”, with knowledge graphs, together with an optimal “curriculum” (this is my term, not the official curriculum learning approach) of pre-training objectives. Their case-studies relate to news generation and document understanding for insurance.


Another talk was by **[Emily M. Bender](https://faculty.washington.edu/ebender/)**, who had a nice interactive format to her talk. First we heard an argument to work against a rush for large-scale models: they centralize power, and are built without specific task or idea in mind - which may make them less suitable for specific tasks. The goal becomes improvement on benchmark metrics, rather than having a  focus on specific problems and task-oriented improvement. As an interactive exercise, small groups of participants received [Envisioning Cards](https://www.envisioningcards.com/?page_id=2) with specific value and responsibilities of  We were encouraged to think of a use-case centralizing this value (for instance, a value of environmentally consciousness) and think of stakeholders, values, and users. Emily then led an interesting and sometimes heated discussion, where some people questioned Emily’s claim that some applications of LLMs - such as automated legal advice or medical uses - should never be used and are inherently harmful. The cards really helped to foster discussion.


# 4. Efficient LLMS: Fine-Tuning and Pre-training

Some talks also focussed on efficient LLMS, and one talk I thought was especially good was by [Ivan Vulić](https://sites.google.com/site/ivanvulic/). He started with “I actually really like creating small models!”: The talk focussed on modularity and parameter-efficiency. The core idea was to not fine-tune entire models, but only updating a small adapter in the model. Interesting is that this allows for compositionality: you can separate language knowledge from task knowledge. He gave the example of a “color” skill and an “animal” recognition skill: combining both should unlock “recognizing the color of animals”. 

Another core idea is that this allows more multi-lingual NLP: it is infeasible to train LLMs for each and every language, and each and every task, but having separate modular adapters for each may be feasible, and makes updating models efficient and perhaps also more able to deal with unseen scenarios. 

One particular interesting idea mentioned was the use of language families in hierarchical adapters, e.g. Indo-European versus Afro-Asiatic languages, for cross-lingual transfer. Another was lexical initialization (e.g. training a separate tokenizer for languages with specific scripts), which hugely improves performance. The talk ended with mentioning the [AdapterHub](https://adapterhub.ml/), where people can share and create adapter components asynchronously.

Ivan's talk then went into great detail on different paradigms and research ideas: I fully got his enthusiasm and the many research directions and developments, but cannot possibly reproduce them here, so please check out his extensive [slides](http://nlpl.eu/skeikampen23/vulic.pdf). 





All in all, this blog post describes some of my personal highlights from the winter school. It only covers the panel and four talks, but in total there were 7 talks. please do check out the [wiki page of the winter school](http://wiki.nlpl.eu/index.php/Community/training), which shows all slides and also more information on the winter school. Sadly, [Anna Rogers](https://annargrs.github.io/) had a planned talk, but due to illness was not able to present. 😞

I hope to be able to go to more such events in the future (maybe also to have more to blog about! 😁)

Best wishes,
Myrthe


