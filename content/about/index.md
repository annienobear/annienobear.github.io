+++
date = '2025-06-26T00:29:48-05:00'
draft = false
title = 'About'
+++

I'm a Computer Science Ph.D. student at the University of Wisconsin–Madison, advised by Prof. [Kassem Fawaz](https://kassemfawaz.com/) in the [Wisconsin Privacy and Security Group](https://wiscprivacy.com/).

My research lies at the intersection of technical HCI, privacy, and AI-driven robotics. I focus on building trustworthy systems that model the complex social dynamics of multi-user environments. By incorporating qualitative methods and social science theories, I develop technologies that respect the complex dynamics of interpersonal relationships and security needs.

## What I work on

My dissertation asks a single question: **is GenAI ready to understand household privacy norms and make privacy decisions on people's behalf — and if not, what would it take to get there?**

Privacy in a home is not an individual setting. Accounts, devices, and now embodied agents are shared by people whose preferences differ, and systems designed for a single user have no good way to negotiate between them. My work runs along three strands.

**Characterizing the threat.** How GenAI actually gets used, mediated, and misused by people who share accounts and devices. I interviewed 12 U.S. families sharing a single ChatGPT account to understand what parents and children get out of it, and how parents mediate it with almost no platform controls to help ([Family Relations 2025](https://onlinelibrary.wiley.com/doi/epdf/10.1111/fare.13171), [arXiv:2504.09004](https://arxiv.org/abs/2504.09004)). I also run participatory design with multi-person households on what a privacy-aware household robot should do.

**Measuring whether GenAI can reason about privacy.** Using Contextual Integrity, I built a benchmark of in-home robot scenarios where 450 people set the human baseline and state-of-the-art LLMs answer the same questions ([arXiv:2507.16124](https://arxiv.org/abs/2507.16124)). The short version: models are not ready to decide on their own — agreement with the person they serve stays low even under the best prompting — but they get sharply better when a human supplies context.

**Building defenses at two levels of autonomy.** That result splits the work in two. A *privacy auditor* detects harms with a human in the loop — for example, a detector that found 1,014 abusable automation recipes among 12,962 public ones, covering surveillance, impersonation, overloading, and lockout in intimate partner violence ([USENIX Security 2025](/abusability-ipv/)). A *privacy controller*, which makes contextual privacy decisions on the device itself, is the proposed direction.

The through-line is turning GenAI from a source of multi-user privacy risk into a defense for the people most exposed to it.

## Talks and coverage

I've presented this work at the [University of Cambridge security seminar](https://www.cl.cam.ac.uk/research/security/seminars/archive/video/2026-02-10-t243715.html) and to threat assessment practitioners at the ATAP Great Lakes Chapter. It has been covered by [WKOW](https://www.wkow.com/news/uw-madison-researchers-find-automation-apps-can-enable-dating-abuse/article_2e61df1f-fb91-40f1-b867-1cde8fc914df.html), [On Wisconsin](https://onwisconsin.uwalumni.com/detecting-and-preventing-digital-abuse/), and the [UW College of Engineering](https://engineering.wisc.edu/news/uw-madison-researchers-expose-how-automation-apps-can-spy-and-how-to-detect-it/).

## Contact

The best way to reach me is email: [hzhang664@wisc.edu](mailto:hzhang664@wisc.edu).
