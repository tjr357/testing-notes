---
id: 3bfbbJQGjSyiEt3bnNiTW
title: Joe's Notes on Acclerate Book
desc: ''
updated: 1645225706336
created: 1645225706336
stub: false
isDir: false
---
My Template
---

_Created at 2019-05-02._
_Last updated at 2019-05-02._




---

# Joe's Notes on Acclerate Book


Accelerate
The Science Behind DevOps: Building and Scaling High Performing Technology Organizations

By Nicole Forsgren, PhD; Jez Humble; Gene Kim

On Culture
The ability to take an experimental approach to product development is highly correlated with the technical practices that contribute to continuous delivery.

In pathological and bureaucratric organizational cultures, measurement is used as a form of control, and people hide information that challenges existing rules, strategies, and power structures.  "Whenever there is fear, you get the wrong numbers" (Deming)

"If I’m not genuinely curious and only show up when there’s a failure, then I am failing as a senior leader. It’s important to build trust and to demonstrate that failure leads to inquiry" - Courtney Kissler, VP Digital Platform Engineering, Nike

Likert-style culture questions to measure culture:

Information is actively sought
Messengers are not punished when they deliver news of failures or other bad news
Responsibilities are shared
Cross-functional collaboration is encouraged and rewarded
Failure causes inquiry
New ideas are welcomed
Failures are treated primarily as opportunities to improve the system
On Ownership and Scaling
Design systems are loosely coupled - that is - can be changed and validated independently of each other.

The goal of a loosely coupled architecture is to ensure that the available communication bandwidth isn’t overwhelmed by fine-grained decision-making at the implementation level, so we can instead use that bandwidth for discussing higher-level shared goals and how to achieve them.

By giving developers the tools to detect problems when they occur, the time and resources to invest in their development, and the authority to fix problems straight away, we create an environment where developers accept responsibility for global outcomes such as quality and stability. If a development team isn’t allowed, without authorization from some outside body, to change requirements or specifications in response to what they discover, their ability to innovate is sharply inhibited.

On Processes and Practices
Agile
Many Agile adoptions have treated technical practices as secondary compared to the management and team practices that some Agile frameworks emphasize.

Our research shows that technical practices play a vital role in achieving these outcomes.

Lean Management Practices
Limiting work in progress (WIP), and using these limits to drive process improvement and increase throughput. WIP limits on their own do not strongly predict delivery performance. It’s only when they’re combined with the use of visual displays and have a feedback loop from production monitoring tools back to delivery teams or the business that we see a strong effect.

Creating and maintaining visual displays showing key quality and productivity metrics and the current status of work (including defects), making these visual displays available to both engineers and leaders, and aligning these metrics with operational goals.

Using data from application performance and infrastructure monitoring tools to make business decisions on a daily basis.

On Communication "Above"
The potential for value delivery and growth within organizations is much greater than executives currently realize.

Executives are especially prone to overestimating their progress when compared to those who are actually doing the work.

There is a clear need to measure DevOps capabilities accurately and to communicate these measurement results to leaders, who can use them to make decisions and inform strategy about their organization’s technology posture.

On Measuring Performance
Meta-Model - what's a good measure of performance look like?
A successful measure of performance should have two key characteristics.

First, it should focus on a global outcome to ensure teams aren’t pitted against each other. The classic example is rewarding developers for throughput and operations for stability.
Second, our measure should focus on outcomes not output: it shouldn’t reward people for putting in large amounts of busywork that doesn’t actually help achieve organizational goals.
A key objective for management is making the state of these system - level outcomes transparent, working with the rest of the organization to set measurable, achievable, time-bound goals for these outcomes, and then helping their teams work toward them.

There have been many attempts to measure the performance of software teams. Most of these measurements focus on productivity. In general, they suffer from two drawbacks:

First, they focus on outputs rather than outcomes.
Second, they focus on individual or local measures rather than team or global ones.
Velocity is designed to be used as a capacity planning tool; for example, it can be used to extrapolate how long it will take the team to complete all the work that has been planned and estimated. However, some managers have also used it as a way to measure team productivity, or even to compare teams.

Measuring Delivery Performance
In our search for measures of delivery performance that meet these criteria , we settled on four:

Delivery Lead Time
Deployment Frequency
Time to Restore Service
Change Fail Rate
Lead Time
The time it takes to go from a customer making a request to the request being satisfied.

In the context of product development, where we aim to satisfy multiple customers in ways they may not anticipate, there are two parts to lead time:

The time it takes to design and validate a product or feature
The time to deliver the feature to customers
In the design part of the lead time, it’s often unclear when to start the clock, and often there is high variability. However, the delivery part of the lead time — the time it takes for work to be implemented, tested, and delivered — is easier to measure and has a lower variability.

Batch Size
Reducing batch size is another central element of the Lean paradigm — indeed , it was one of the keys to the success of the Toyota production system.

Reducing batch sizes:

Reduces cycle times and variability in flow
Accelerates feedback
Reduces risk and overhead
Improves efficiency
Increases motivation and urgency
Reduces costs and schedule growth
In software, batch size is hard to measure and communicate across contexts as there is no visible inventory. Therefore, we settled on deployment frequency as a proxy for batch size since it is easy to measure and typically has low variability.

Time to Restore Service
In modern software products and services, which are rapidly changing complex systems, failure is inevitable, so the key question becomes: How quickly can service be restored?

Change Fail Rate
What percentage of changes to production (including, for example, software releases and infrastructure configuration changes) fail? In the context of Lean, this is the same as percent complete and accurate for the product delivery process, and is a key quality metric.

We asked respondents what percentage of changes for the primary application or service they work on either result in degraded service or subsequently require remediation (e.g., lead to service impairment or outage, require a hotfix, a rollback, a fix - forward, or a patch)

Findings
When compared to low performers, the high performers have:

46 times more frequent code deployments
440 times faster lead time from commit to deploy
170 times faster mean time to recover from downtime
5 times lower change failure rate ( 1 / 5 as likely for a change to fail )
Analysis showed that only lead time, release frequency, and time to restore together form a valid and reliable construct. Thus, in the rest of book, when we talk about software delivery performance it is defined using only the combination of those three metrics.

Measuring Quality
Quality and performance of applications, as perceived by those working on them

% of time spent on rework or unplanned work
Unplanned work and rework are useful proxies for quality because they represent a failure to build quality into our products
% of time spent working on defects identified by end users
Having automated tests primarily created and maintained either by QA or an outsourced party is not correlated with IT performance.

