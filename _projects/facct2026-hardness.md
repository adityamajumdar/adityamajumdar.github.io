---
layout: page
title: "Why AI Built to Help Gets Shelved"
description: "A blog post on the barriers preventing AI for Social Impact projects from reaching deployment."
img:
importance: 1
category: work
---

Imagine a team of researchers spending two years building an AI system to help epidemiologists decide who to test during a disease outbreak. The model works. The results look good. The paper gets published. And then nothing. The system never reaches a clinic, never informs a single decision, never helps a single patient.

This isn't a hypothetical. It is one of the stories we heard while conducting research for our [FAccT 2026 paper](https://arxiv.org/abs/2506.14829). And it was not the only one.

A recent [study](https://www.mckinsey.com/~/media/mckinsey/business%20functions/quantumblack/our%20insights/ai%20for%20social%20good/2024/ai-for-social-good-improving-lives-and-protecting-the-planet-v2.pdf) showed that between 2018 and 2023, the number of AI for Social Impact (AI4SI) projects tripled from 170 to over 600. These are projects applying machine learning to problems like HIV prevention, maternal health, food insecurity, wildlife conservation, and disaster response. Work explicitly oriented toward communities that large technology companies have little incentive to serve. Yet a striking majority of these projects never reach the people they were designed for.

<div class="row mt-4 mb-2">
  <div class="col-sm-12">
    <svg viewBox="0 0 680 180" xmlns="http://www.w3.org/2000/svg" style="width:100%;height:auto;">
      <rect width="680" height="180" fill="#EAF3F4" rx="8"/>
      <text x="50" y="42" font-family="Georgia,serif" font-size="13" fill="#5A6A7A" font-weight="600">Of 600+ AI4SI projects studied (2018-2023):</text>
      <rect x="50" y="58" width="580" height="48" rx="4" fill="#D6DFE8"/>
      <rect x="50" y="58" width="418" height="48" rx="4" fill="#E05C3A"/>
      <text x="65" y="89" font-family="Georgia,serif" font-size="22" font-weight="700" fill="white">72% -- never left R&amp;D</text>
      <text x="535" y="89" font-family="Georgia,serif" font-size="13" fill="#5A6A7A" text-anchor="middle">28%</text>
      <rect x="50" y="126" width="12" height="12" fill="#E05C3A" rx="2"/>
      <text x="68" y="137" font-family="sans-serif" font-size="12" fill="#2C2C2C">Stalled at proof-of-concept or R&amp;D phase</text>
      <rect x="300" y="126" width="12" height="12" fill="#D6DFE8" rx="2"/>
      <text x="318" y="137" font-family="sans-serif" font-size="12" fill="#2C2C2C">Reached real-world deployment</text>
      <text x="50" y="165" font-family="sans-serif" font-size="10" fill="#8096AE" font-style="italic">Source: Bankhwal et al. (2024), McKinsey Digital.</text>
    </svg>
    <p class="text-center" style="font-size:0.85rem;color:#666;margin-top:0.5rem;"><em>Despite rapid growth in AI for Social Impact, most projects stall before reaching the communities they were built to serve.</em></p>
  </div>
</div>

So what is going wrong? Our research set out to answer that question, not from the perspective of the nonprofits or communities being served (others have studied that), but from the researchers themselves. We interviewed 26 active AI4SI researchers, covering 38 projects across public health, conservation, social justice, and agriculture. Almost all of them had a project that never made it out of the lab. What we found was that deployment failure is rarely about the technology. It is about everything surrounding it.

## The Gauntlet

By reading through our interview transcripts and grouping what we heard into patterns, we identified four interconnected categories of challenges. Think of them as a gauntlet: a technically excellent project has to survive all four.

<div class="row mt-4 mb-2">
  <div class="col-sm-12">
    <svg viewBox="0 0 680 200" xmlns="http://www.w3.org/2000/svg" style="width:100%;height:auto;">
      <rect width="680" height="200" fill="#F7F4EF" rx="8"/>
      <defs>
        <marker id="arr" markerWidth="8" markerHeight="7" refX="7" refY="3.5" orient="auto">
          <path d="M0,0 L0,7 L8,3.5 z" fill="#B0C4D4"/>
        </marker>
      </defs>
      <rect x="28" y="50" width="138" height="118" rx="6" fill="#1B2A4A"/>
      <text x="97" y="80" font-family="Georgia,serif" font-size="11.5" fill="#7BBFCC" text-anchor="middle" font-weight="700">STRUCTURAL</text>
      <text x="97" y="99"  font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Publish-or-perish</text>
      <text x="97" y="114" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Funding shortfalls</text>
      <text x="97" y="129" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Institutional red tape</text>
      <text x="97" y="144" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Reward mismatches</text>
      <line x1="169" y1="109" x2="186" y2="109" stroke="#B0C4D4" stroke-width="2" marker-end="url(#arr)"/>
      <rect x="189" y="50" width="138" height="118" rx="6" fill="#0D7680"/>
      <text x="258" y="80" font-family="Georgia,serif" font-size="11.5" fill="white" text-anchor="middle" font-weight="700">COMMUNICATION</text>
      <text x="258" y="99"  font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">AI misconceptions</text>
      <text x="258" y="114" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Different vocabularies</text>
      <text x="258" y="129" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Missing champions</text>
      <text x="258" y="144" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Expectation gaps</text>
      <line x1="330" y1="109" x2="347" y2="109" stroke="#B0C4D4" stroke-width="2" marker-end="url(#arr)"/>
      <rect x="350" y="50" width="138" height="118" rx="6" fill="#4A6080"/>
      <text x="419" y="80" font-family="Georgia,serif" font-size="11.5" fill="white" text-anchor="middle" font-weight="700">COLLABORATION</text>
      <text x="419" y="99"  font-family="sans-serif" font-size="10" fill="#D6DFE8" text-anchor="middle">Trust building</text>
      <text x="419" y="114" font-family="sans-serif" font-size="10" fill="#D6DFE8" text-anchor="middle">Leadership buy-in</text>
      <text x="419" y="129" font-family="sans-serif" font-size="10" fill="#D6DFE8" text-anchor="middle">Territorial dynamics</text>
      <text x="419" y="144" font-family="sans-serif" font-size="10" fill="#D6DFE8" text-anchor="middle">Network gatekeeping</text>
      <line x1="491" y1="109" x2="508" y2="109" stroke="#B0C4D4" stroke-width="2" marker-end="url(#arr)"/>
      <rect x="511" y="50" width="138" height="118" rx="6" fill="#E05C3A"/>
      <text x="580" y="80" font-family="Georgia,serif" font-size="11.5" fill="white" text-anchor="middle" font-weight="700">OPERATIONAL</text>
      <text x="580" y="99"  font-family="sans-serif" font-size="10" fill="#FDD5C8" text-anchor="middle">Shifting environments</text>
      <text x="580" y="114" font-family="sans-serif" font-size="10" fill="#FDD5C8" text-anchor="middle">Data access</text>
      <text x="580" y="129" font-family="sans-serif" font-size="10" fill="#FDD5C8" text-anchor="middle">Scaling up</text>
      <text x="580" y="144" font-family="sans-serif" font-size="10" fill="#FDD5C8" text-anchor="middle">Keeping it running</text>
      <text x="340" y="186" font-family="sans-serif" font-size="10.5" fill="#8096AE" text-anchor="middle" font-style="italic">Each barrier must be cleared for a project to reach deployment. Most don't make it through all four.</text>
    </svg>
    <p class="text-center" style="font-size:0.85rem;color:#666;margin-top:0.5rem;"><em>Four barriers that stood between a working AI system and the communities it was built to serve, drawn from interviews with 26 researchers across 38 projects.</em></p>
  </div>
</div>

## The Academic Trap

The structural challenges hit hardest and earliest, and they start inside universities.

Academia runs on a "publish or perish" logic that rewards frequent, new and clever technical contributions. AI4SI work is almost the inverse: slow, full of unglamorous software work, and often producing exactly one paper after two years of fieldwork. One participant described the bind clearly: *"As a PhD student, you may be forced into engineering work for months with no clear roadmap to getting a paper. This is a true blocking factor."*

The pressure shapes behavior in subtle ways too. Several participants described having to dress up applied field work as methods papers, stuffing in unnecessary technical additions just to satisfy reviewers who expected novelty. As one put it: *"The only way to do this was to smuggle it in by writing a methods paper and then putting in the field work as an application. But that meant spending a lot more effort adding unnecessary improvements to things that really were not that useful."* The actual impact got buried in the footnotes.

It is worth pausing on what this means in practice. A PhD student working on AI for HIV prevention might spend eighteen months building and testing a system with a partner clinic. A peer working on a purely technical problem might publish three papers in the same period. Academic hiring committees, grant panels, and tenure reviews still largely evaluate people on publication counts. The researcher doing the harder, slower, more important work often looks less productive on paper. That is not a personal failing. It is a structural one.

## What Partner Organizations Are Actually Dealing With

Even researchers willing to absorb that cost still face the partner organization side of the equation. Nonprofits, government agencies, and community health organizations typically operate with small teams, stretched budgets, and no official mandate to run multi-year AI research collaborations. Participating in a project is usually on top of their actual job, unpaid, and voluntary.

This matters because sustained engagement requires sustained time. Getting data together, reviewing outputs, attending check-ins, signing off on decisions: all of it takes hours that nonprofit staff and volunteers often do not have to spare. When the collaboration slows down or stalls, it is not because people stopped caring. It is because the capacity was never really there to begin with.

And when it comes to buy-in, the picture gets more complicated. One participant, reflecting on a wildlife conservation project, recalled a moment that stuck with us:

> "A high-level secretary said, sounds like an awesome idea, let's do it! But then, when we went to the rangers on the ground, they said, we just need better shoes. We just need better guns. We don't need AI."

This captures something that most conversations about AI consistently miss. The mismatch in what each side is rewarded for is not just between academia and its partners. It exists *within* organizations too. Leadership enthusiasm can mask real frontline resistance, and a better algorithm does nothing to bridge that gap. The people who will actually use a system day-to-day often were not consulted when the collaboration was agreed to, and they have their own judgment about what would actually help.

## The Slow Work of Building Trust

Beneath the structural and organizational barriers lies something harder to measure: trust. Partner organizations have often been burned before. A university team shows up, collects data, runs some interviews, publishes a paper, and disappears. The community was promised something useful and got an acknowledgments section. After a few rounds of this, organizations become understandably cautious. As one researcher put it: *"They don't trust you because they feel like you just come and get a paper, and then you're gone."*

Building trust takes time and it takes proof. The researchers who had actually managed to deploy something shared a consistent early strategy: deliver something useful before the heavy technical work begins. Not a prototype, not a demo, but something genuinely helpful to the partner right now. A simple chart showing patterns in their own data. A quick statistical analysis answering a question they had been sitting on. Something that demonstrates you understand their work and are there to help with it, not just to study it.

One participant described routinely spending the first three months of a collaboration doing exactly this, delivering a data visualization or a simple analysis before any modeling work started. It kept partners engaged and interested. It also helped the research team understand the problem well enough to actually solve it.

Data itself presents its own obstacle course. One participant spent six months helping a partner organization figure out what data they even had, only to discover that the data the project needed had never been collected. Another spent a full year building enough trust for a partner to share sensitive records, eventually embedding a student as an intern at the organization just to make the data access physically possible. These are not edge cases. They are the norm.

Communication is another persistent source of friction. AI means very different things to different people. A nonprofit working in public health may worry about surveillance, bias, or being replaced. A researcher trying to explain a scheduling algorithm is talking about something entirely different, but the word AI triggers the same anxieties. *"The kind of AI they're worried about is not the kind I'm talking about,"* one participant noted. *"And it takes a while to sort that out, because they don't know what to ask for, and we don't know enough about their domain to tell them what they should be asking."* Long relationships help. Quick handoffs do not.

## The Maintenance Problem Nobody Talks About

Even the projects that do reach deployment face a final, underappreciated challenge: staying deployed. Academic labs are not built for software maintenance. Students graduate. Grants expire. The one person who understood how the system worked moves on to their next position. And unlike a consumer app that generates revenue and has a team of engineers, these systems often serve small, low-resource communities where business models simply do not apply.

> "If funding is not figured out, it may not fail immediately, but it will fail eventually. Because at the end of the day, somebody has to pay for it."

<div class="row mt-4 mb-2">
  <div class="col-sm-12">
    <svg viewBox="0 0 680 110" xmlns="http://www.w3.org/2000/svg" style="width:100%;height:auto;">
      <rect width="680" height="110" fill="#1B2A4A" rx="8"/>
      <text x="340" y="42" font-family="Georgia,serif" font-size="36" font-weight="700" fill="#E05C3A" text-anchor="middle">55%</text>
      <text x="340" y="64" font-family="Georgia,serif" font-size="14" fill="white" text-anchor="middle">of AI4SI projects receive less than $250,000 in total funding</text>
      <text x="340" y="85" font-family="sans-serif" font-size="12" fill="#7BBFCC" text-anchor="middle">Yet keeping a deployed system running can require millions in engineering and infrastructure.</text>
      <text x="340" y="102" font-family="sans-serif" font-size="10" fill="#4A6080" text-anchor="middle" font-style="italic">Source: Bankhwal et al. (2024)</text>
    </svg>
    <p class="text-center" style="font-size:0.85rem;color:#666;margin-top:0.5rem;"><em>The gap between what a research grant provides and what keeping a system running actually costs is rarely acknowledged, and rarely closed.</em></p>
  </div>
</div>

There is also a subtler version of this problem. Even when a system is technically still running, the environment around it keeps changing. Staff turn over at partner organizations. Policies shift. The problem the system was built to solve gets reframed. One participant described how an industry partner rapidly redirected all their attention to generative AI after ChatGPT launched, deprioritizing an ongoing collaboration mid-project. Another described a system that had worked well in the context it was designed for, but became increasingly ill-suited as the partner organization evolved. The software stayed the same. Everything else moved.

## What Actually Helps

Our participants were not only documenting failure. Many had found things that genuinely worked, and a few patterns came up consistently enough to be worth naming.

The strategy mentioned most often was what several researchers called the **"quick win."** In the early weeks of a new collaboration, before any serious technical work begins, prioritize delivering something immediately useful to the partner. A visualization of their own data. A short analysis answering a question they have been sitting on. Something that shows you understand their work, demonstrates your intentions are good, and gives them a reason to keep showing up to meetings. It builds credibility, and it sharpens your own understanding of what actually needs solving.

Working through **go-betweens** dramatically accelerated deployment in several cases. These are researchers from social work, public health, or medicine who already have long-standing relationships with partner organizations. They know the right people, understand the institutional culture, and can vouch for the research team in ways that no cold email can replicate. One participant described a collaboration where a social work research team handled all partner-facing interactions while the AI team focused on the technical work. The combination got a system deployed that likely would not have made it otherwise.

The tradeoff is worth naming: this creates a two-tier structure where well-connected researchers can move faster and reach more partners, while newer researchers without those networks find themselves excluded from conversations that run on pre-existing trust. That is a problem worth fixing at the field level, not just navigating around individually.

At the institutional level, participants pointed to structural changes that could actually move things: recognizing deployed systems and open-source tools as legitimate research contributions (not just papers), building university-level offices or consortia to help with data agreements and partner outreach, and developing training programs that give AI researchers genuine exposure to fieldwork and statistics and the experience of working directly with communities.

Some funding agencies are already experimenting with this. Programs like NSF CIVIC and NSF TTP fund early-stage collaborations where researchers and partners work together to define the problem before committing to a full project. The idea is to build the relationship and surface mismatches early, when adjustments are cheap, rather than discovering two years in that the partner needed something entirely different.

## Why This Matters

The communities that this research aims to serve, people experiencing homelessness, subsistence farmers, patients in under-resourced clinics, are not going to be served by large technology companies. Those communities are not profitable markets. AI built to help them requires researchers who are willing to do slow, hard, relationship-dependent work for modest academic reward. It requires partners who are willing to invest time they do not have. And it requires institutions and funders to value outcomes that do not fit neatly into a publication count.

The problems we document in this paper are not new to anyone working in this field. But they have rarely been laid out systematically from the researcher's own perspective. We hope that naming the gauntlet clearly makes it slightly easier to navigate, and that the AI systems built to help people actually get to do so.

---

*Based on: Majumdar, Zhang, Prawal & Yadav. "The Hardness of Achieving Impact in AI for Social Impact Research." FAccT '26, Montreal.*