---
layout: page
title: "Why AI Built to Help Gets Shelved"
description: "A blog post on the structural barriers preventing AI for Social Impact projects from reaching deployment. Based on our FAccT 2026 paper."
img:
importance: 1
category: work
---

Between 2018 and 2023, the number of AI for Social Impact (AI4SI) projects tripled from 170 to over 600. These are projects applying machine learning to problems like HIV prevention, maternal health, food insecurity, and disaster response — work explicitly oriented toward communities that large tech companies have little incentive to serve. Yet a striking majority of these projects never reach the communities they're designed for.

For our [FAccT 2026 paper](https://doi.org/10.1145/3805689.3812387), we interviewed 26 active AI4SI researchers covering 38 projects across public health, conservation, social justice, and agriculture. Almost all of them had a project that never made it out of the lab. We set out to understand why — not from the perspective of the nonprofits or communities being served, but from the researchers themselves.

<div class="row mt-4 mb-2">
  <div class="col-sm-12">
    <svg viewBox="0 0 680 180" xmlns="http://www.w3.org/2000/svg" style="width:100%;height:auto;">
      <rect width="680" height="180" fill="#EAF3F4" rx="8"/>
      <text x="50" y="42" font-family="Georgia,serif" font-size="13" fill="#5A6A7A" font-weight="600">Of 600+ AI4SI projects studied (2018–2023):</text>
      <rect x="50" y="58" width="580" height="48" rx="4" fill="#D6DFE8"/>
      <rect x="50" y="58" width="418" height="48" rx="4" fill="#E05C3A"/>
      <text x="65" y="89" font-family="Georgia,serif" font-size="22" font-weight="700" fill="white">72% — never left R&amp;D</text>
      <text x="535" y="89" font-family="Georgia,serif" font-size="13" fill="#5A6A7A" text-anchor="middle">28%</text>
      <rect x="50" y="126" width="12" height="12" fill="#E05C3A" rx="2"/>
      <text x="68" y="137" font-family="sans-serif" font-size="12" fill="#2C2C2C">Stalled at proof-of-concept or R&amp;D phase</text>
      <rect x="300" y="126" width="12" height="12" fill="#D6DFE8" rx="2"/>
      <text x="318" y="137" font-family="sans-serif" font-size="12" fill="#2C2C2C">Reached real-world deployment</text>
      <text x="50" y="165" font-family="sans-serif" font-size="10" fill="#8096AE" font-style="italic">Source: Bankhwal et al. (2024), McKinsey Digital.</text>
    </svg>
    <p class="text-center" style="font-size:0.85rem;color:#666;margin-top:0.5rem;"><em>Despite rapid growth in AI for Social Impact, most projects stall before reaching the communities they intend to serve.</em></p>
  </div>
</div>

What we found was that deployment failure is rarely about the technology. It's about everything surrounding it.

## The Gauntlet

Through the analysis of our interviews, we identified four interconnected categories of challenges. Think of them as a gauntlet: a technically excellent project has to survive all four.

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
      <text x="97" y="129" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Institutional inertia</text>
      <text x="97" y="144" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Misaligned incentives</text>
      <line x1="169" y1="109" x2="186" y2="109" stroke="#B0C4D4" stroke-width="2" marker-end="url(#arr)"/>
      <rect x="189" y="50" width="138" height="118" rx="6" fill="#0D7680"/>
      <text x="258" y="80" font-family="Georgia,serif" font-size="11.5" fill="white" text-anchor="middle" font-weight="700">COMMUNICATION</text>
      <text x="258" y="99"  font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">AI misconceptions</text>
      <text x="258" y="114" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Disciplinary jargon</text>
      <text x="258" y="129" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Missing champions</text>
      <text x="258" y="144" font-family="sans-serif" font-size="10" fill="#AEDCE8" text-anchor="middle">Expectation gaps</text>
      <line x1="330" y1="109" x2="347" y2="109" stroke="#B0C4D4" stroke-width="2" marker-end="url(#arr)"/>
      <rect x="350" y="50" width="138" height="118" rx="6" fill="#4A6080"/>
      <text x="419" y="80" font-family="Georgia,serif" font-size="11.5" fill="white" text-anchor="middle" font-weight="700">COLLABORATION</text>
      <text x="419" y="99"  font-family="sans-serif" font-size="10" fill="#D6DFE8" text-anchor="middle">Trust building</text>
      <text x="419" y="114" font-family="sans-serif" font-size="10" fill="#D6DFE8" text-anchor="middle">Leadership buy-in</text>
      <text x="419" y="129" font-family="sans-serif" font-size="10" fill="#D6DFE8" text-anchor="middle">Territorial dynamics</text>
      <text x="419" y="144" font-family="sans-serif" font-size="10" fill="#D6DFE8" text-anchor="middle">Intermediary access</text>
      <line x1="491" y1="109" x2="508" y2="109" stroke="#B0C4D4" stroke-width="2" marker-end="url(#arr)"/>
      <rect x="511" y="50" width="138" height="118" rx="6" fill="#E05C3A"/>
      <text x="580" y="80" font-family="Georgia,serif" font-size="11.5" fill="white" text-anchor="middle" font-weight="700">OPERATIONAL</text>
      <text x="580" y="99"  font-family="sans-serif" font-size="10" fill="#FDD5C8" text-anchor="middle">Dynamic environments</text>
      <text x="580" y="114" font-family="sans-serif" font-size="10" fill="#FDD5C8" text-anchor="middle">Data access</text>
      <text x="580" y="129" font-family="sans-serif" font-size="10" fill="#FDD5C8" text-anchor="middle">Scalability</text>
      <text x="580" y="144" font-family="sans-serif" font-size="10" fill="#FDD5C8" text-anchor="middle">Maintenance burden</text>
      <text x="340" y="186" font-family="sans-serif" font-size="10.5" fill="#8096AE" text-anchor="middle" font-style="italic">Each barrier must be cleared for a project to reach deployment. Most don't make it through all four.</text>
    </svg>
    <p class="text-center" style="font-size:0.85rem;color:#666;margin-top:0.5rem;"><em>Four challenge categories identified through thematic analysis of 26 researcher interviews covering 38 AI4SI projects.</em></p>
  </div>
</div>

The structural challenges hit hardest and earliest. Academia runs on a "publish or perish" logic that rewards frequent, technically novel output. AI4SI work is almost the inverse: slow, iterative, engineering-heavy, and often producing exactly one paper after two years of fieldwork. One participant put it directly: *"As a PhD student, you may be forced into engineering work for months with no clear roadmap to getting a paper. This is a true blocking factor."*

But even researchers willing to absorb that cost still face the partner organization side of the equation. Nonprofits and government agencies typically operate with small teams, limited budgets, and no mandate for multi-year AI research collaborations. And when a senior administrator says "this sounds great, let's do it," that enthusiasm doesn't always reach the frontline. One participant, reflecting on a wildlife conservation project, recalled:

> "A high-level secretary said, 'sounds like an awesome idea, let's do it!' But then, when we went to the rangers on the ground, they said, 'we just need better shoes. We just need better guns. We don't need AI.'"

This captures something the broader AI discourse consistently misses: the problem of misaligned incentives isn't just between academia and its partners — it exists *within* organizations. Leadership enthusiasm can mask real frontline resistance, and no amount of technical sophistication bridges that gap.

## The Slow Work of Building Trust

Beneath the structural and organizational barriers lies something harder to quantify: trust. Partner organizations have often been burned before. A university team shows up, runs interviews, publishes a paper, and disappears. As one researcher put it: *"They don't trust you because they feel like you just come and get a paper, and then you're gone."*

The researchers who had actually managed to deploy something shared a consistent strategy: deliver something useful *early*, before the heavy technical work begins. A simple data visualization. A regression model answering a question the partner actually had. Something tangible that demonstrates commitment — not just with leadership, but with the people who will eventually use the system.

Data, too, is its own obstacle course. One participant spent six months helping a partner organization figure out what data they even had — only to discover that the data needed for the project had never been collected. Another spent a full year building sufficient trust before a partner would share sensitive records, eventually embedding a student as an intern just to make data access logistically possible.

## The Maintenance Problem Nobody Talks About

Even the projects that reach deployment face a final, underappreciated challenge: staying deployed. Academic labs are not built for software maintenance. Students graduate. Grants expire. The one person who understood the system moves on.

> "If funding is not figured out, it may not fail immediately — but it will fail eventually. Because at the end of the day, somebody has to pay for it."

<div class="row mt-4 mb-2">
  <div class="col-sm-12">
    <svg viewBox="0 0 680 110" xmlns="http://www.w3.org/2000/svg" style="width:100%;height:auto;">
      <rect width="680" height="110" fill="#1B2A4A" rx="8"/>
      <text x="340" y="42" font-family="Georgia,serif" font-size="36" font-weight="700" fill="#E05C3A" text-anchor="middle">55%</text>
      <text x="340" y="64" font-family="Georgia,serif" font-size="14" fill="white" text-anchor="middle">of AI4SI projects receive less than $250,000 in total funding</text>
      <text x="340" y="85" font-family="sans-serif" font-size="12" fill="#7BBFCC" text-anchor="middle">Yet scaling a deployed system can require millions in engineering and infrastructure.</text>
      <text x="340" y="102" font-family="sans-serif" font-size="10" fill="#4A6080" text-anchor="middle" font-style="italic">Source: Bankhwal et al. (2024)</text>
    </svg>
    <p class="text-center" style="font-size:0.85rem;color:#666;margin-top:0.5rem;"><em>The gap between what research grants provide and what sustainable deployment actually costs is rarely acknowledged.</em></p>
  </div>
</div>

## What Actually Helps

Our participants weren't only documenting failure. A few strategies emerged consistently across interviews.

The most universally cited was the **"quick win"**: in the early weeks of a collaboration, prioritize delivering something immediately useful to the partner before any heavy technical work begins. It builds trust, sharpens the problem definition, and signals that you're not just there to extract data for a paper.

Working through **intermediaries** — researchers from social work, medicine, or public health who already hold long-standing relationships with partner organizations — dramatically accelerated deployment in several cases. The tradeoff is real: this creates an access problem for early-career researchers who don't yet have those networks.

At the institutional level, participants pointed to structural reforms: recognizing deployed systems and open-source tools as legitimate research outputs, building university consortia to manage data agreements and partner matching, and developing training programs that give AI researchers genuine exposure to fieldwork and community-engaged methods.

## Why This Matters

The communities that AI4SI research aims to serve are not going to be served by large technology companies. Those communities are not profitable markets. AI4SI is, in a real sense, the only part of the AI ecosystem explicitly oriented toward them. That makes getting this right urgent.

By naming the gauntlet clearly, we hope to make it slightly less lethal — and to help ensure that the AI systems built to help people actually get to do so.

---

*Based on: Majumdar, Zhang, Prawal & Yadav. "The Hardness of Achieving Impact in AI for Social Impact Research." FAccT '26, Montreal. [doi.org/10.1145/3805689.3812387](https://doi.org/10.1145/3805689.3812387). Supported by NSF Grant #2427737.*