---
title: "Voter Data Security report (Purple Tornado, Q1 2019)"
categories: 
  - blog
  - purpletornado
type: "blog"  
layout: single
author_profile: true
read_time: true
comments: true
share: true
related: true
description: >
  An overview of my work with Purple Tornado on the U.S. Voter Data Security report commissioned by DHS in 2018.
excerpt: >
  An overview of my work with Purple Tornado on the U.S. Voter Data Security report commissioned by DHS in 2018.
---

(Note: A version of this essay appears on the [Purple Tornado blog](http://www.medium.com/in-present-tense/).)

As part of our software futures research grant from the Department of Homeland Security, Science and Technology directorate, the Purple Tornado team spent a few months familiarizing ourselves with an issue that might be called an open wound in North American politics: the security and integrity of the ballot. I’ll recount here some highlights and then explain the final form taken by our public-domain report, linked below.

## Research Scope and Methods

[![cover of report](/assets/images/vds_report_cover.png){: .align-center}](http://bit.ly/VDSreport)

Electronic voting or blockchain voting were out of scope right out the gate, for reasons that came up extemporaneously in our interviews: namely, that no experts we talked to seemed to think either would be even remotely secure enough to consider for real elections any time soon. Voting machines themselves were also out of scope, given that multiple other grant-funded research teams were already working specifically on the security of the machines currently licensed for sale in the US and still others teams were designing and testing machines being proposed for future licensing.

Even given that scope, we were surprised by just how much diversity and variation there was between states, how many different kinds of sensitive data there was to protect, and how lively were the debates between experts within it. In fact, we learned there are very few voters in America whose votes are counted exclusively by human beings — in the vast majority, ballot counting processes in “paper-only” states (and their registration information) were rich in digital complexities and attack surfaces. I was grateful for Heather’s cybersecurity perspective, Josh’s experience with intelligence and government information flows, and Kaliya’s expertise in privacy law and best practices as we navigated the contentious waters of election-system funding, voter roll data, and registration data.

We had initially intended to do state by state comparisons, but realized that the bipartisan think tank Center for American Progress had already recently concluded a state by state [comparison of electoral processes](https://www.americanprogress.org/issues/democracy/reports/2018/02/12/446336/election-security-50-states/) with a holistic approach, on allowed our more technically-focused comparison to proceed more anecdotally. Instead, we talked primarily with activists, academics, and software engineers who had worked across multiple states to drill in to trends and recurring problems. Over and over again, they told us that all the technical and process pieces were there, just not the manufacturer cooperation, the cohesion, and the political will to let the experts fix the problems and guide the investments to where they are most needed to advance technology with an eye to data security and integrity.

## Highlights and Surprises

![administrator icon](/assets/images/admin.png){: .align-left}

Personally, my biggest counter-intuitive surprise as a newcomer to the electoral space was the odd mismatch of funding and attention: seemingly, the heavy lifting of both running administrations and reforming them fell to people doing it for altruistic purposes beyond the scope of their actual job duties. The bulk of on-the-ground election administration is done by local civil servants focused on other duties 10 months of every year, countless volunteers, and, I can’t stress this enough, a handful of saints. Elections, and even more so the campaigns leading up them, are run like short-lived startups or volunteer firefighting teams, quickly staffed and unceremoniously disbanded a few days after they’ve delivered their payload. That organizational principle creates its own data issues and attack surfaces, and any attempt at securing election data or reforming the election system has to take into consideration that “no one is answering the customer service line”.

Another high-level finding was that the lion’s share of contracts for hardware and services are held by three companies which effectively have a lock on the federal **certification process** required to legally sell voting machinery to states. One of the simplest and most effective legal hacks to speed up innovation and technical advances in the sector, many speculated, would be to simplify and open up the certification process to allow more competition in this critical infrastructural niche. Few had hopes that this kind of hack would make it through the current Congress, though, or for that matter any imaginable Congress, given the incentives and loyalties at play. Others with ties to the DefCon community fantasized about earmarking a portion of such contracts or certification processes to fund bug bounties, pegging certification to demonstrable security rather than to abstract criteria. Failing such a bold intervention, however, the price of entry has remained high enough to see no significant newcomers in over a decade. Hopefully that’s changing this year due to some civic-minded investments and advocacy.

![scary graphic of election hacking](/assets/images/ballot_hack_graphic.jpg){: .full}

Each headline with the words “hack” and “election” in it is a security event whether any hacking took place or not.
{: .fs-1 .text-center}

Another perspective-altering theme that kept coming up in interviews was that the **perception** of hacking might well be as effective as the most sophisticated hacks. Weakening public trust in the electoral process itself is an effective way to swing tight elections (particularly since young voters and other “swing”demographics are most likely to be dissuaded from voting). What’s more, many geopolitical activists have been arguing for years that the weakening of trust in broad, coalition-based political institutions (the UN, the EU, NATO, and free trade blocs) is, in and of itself, a guiding principle of many powerful states’ foreign policies, which they discuss openly in internal documents and budgets. For this reason, many experts are deeply suspicious of journalists or researchers with a commercial incentive to hyperbolize theoretical threats or dwell on worst-case-scenario speculation, since the average voter is already dangerously demoralized and skeptical about democratic processes thanks to years of sensational press and fear-mongering security contractors drumming up business. As one expert put it, there are very real threats and easily-identified bad actors, but the former have more to do with human error and labor-force education, and the latter are obstructing funding and reform, not hacking databases.

## Final Form

One other recurring theme in our interviews was a cultural divide between two demographics working together closely in the space: on the one hand, elections specialists who tend to have little training or familiarity with data security, and on the other, data specialists with years of experience in public- or private-sector data systems and processes but limited exposure to the esoteric and *sui generis* processes of elections. This informed how we structured our report — we wanted to lay out an actionable agenda regardless of how much budget or staffing the federal elections agencies had, which would be educational in equal parts to both demographics.

![massive infographic of data moving through voting system](/assets/images/vds_diagram_purpletornado.png){: .align-center}

We started by sketching out the current state of the field for the unfamiliar reader, and introducing some of the specialized vocabulary needed to understand technical reports linked from the appendix. Then we proceeded to explain as succinctly as possible all the moving parts in the election system from a data integrity perspective— the diagram above only covers about 2/3 of them!

From there, we tried to describe all the different vulnerabilities inherent to this system as it’s currently built and legislated. This was my favorite part of the process, applying a holistic view and ranking these vulnerabilities by their effects and costs. From here, we outlined an agenda for resilience following the directives and terminology set out for DHS by then-director Nielsen. This included plenty of low-hanging fruit as well as long-term investments and policy-shifts needed to bring our 56 voting systems up to a level of sophistication and defensive monitoring appropriate to critical infrastructure.

In many cases, the low-hanging fruit simply entails convincing the relevant state administrations to listen to and cooperate with experts who are already doing great work in state after state, requiring little or no additional funding from the states. A great example of this was [Democracy Works](http://democracy.works), an education profit that made abundant educational materials available to election administrators and even facilitated information-sharing and co-education between them, free of charge. There are similarly free, open-source repositories of [election software](https://electiontools.org/) and user-experience [design templates](https://www.usability.gov/how-to-and-tools/index.html) maximizing usability (*cough, cough, hanging chads*) and accessibility (something more heavily mandated in public-sector information technology than in the private sector). The listing of key nonprofits and government agencies working in the space was inspiring to compile, particularly knowing that it was probably not comprehensive and that countless other groups are doing God’s work at regional and state levels. The appendix of selected bibliography offers a collection of rabbit-holes allowing anyone new to the space to bring themselves up to speed on elections, state-by-state variations, and the finer points in data integrity and voting data.

The report was released to the public domain in Spring 2019, and is available at [bit.ly/VDSreport](http://bit.ly/VDSreport) (email registration required) from Purple Tornado.
