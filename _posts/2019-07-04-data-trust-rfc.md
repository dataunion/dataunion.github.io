---
layout: post
title:  "Data Trusts - Request For Comments"
date: 2019-07-04 14:08:11 +0200
categories: privacy consent
description: In this RFC we present our concept of a data trust as one way to overcome the main challenges of data custody and to provide a way to make data available for the common good while safeguarding our various privacies.
image: data.jpg 
authors:
 - all
---

- Executive summary
- What comments are we looking for?
- [Link to the full document](https://docs.google.com/document/d/1e-PHibsPE-b4irLPzPmCJenlDTKf34EWljg0wF2Pizo/edit?usp=sharing)

## Executive Summary 

In this RFC we present our concept of a data trust as one way to overcome the main challenges of data custody and to provide a way to make data available for the common good while safeguarding our various privacies.

When it comes to the custody of data about us, we are faced with a plethora of failure modes. In a race to collect ever growing piles of data, corporations and governments have failed to make this data available to the common good and instead weaponized, exploited and enclosed it. Unfortunately, privacy policies coming into force today only address part of the problem. They focus on protecting a strict notion of individual privacy, without concern for the negative externalities to society at large of both over- and under-sharing data. Individuals, meanwhile, are faced with false choices - having to decide between opting into inappropriately permissive terms and conditions or leaving their networks of friends behind - and incomprehensible, obtrusive consent banners. Finally, enclosure of data mostly leaves us unable to challenge claims about us and add missing data to existing datasets, we are bound to create biased artificial intelligences.

### The Data Trust
In our view, any meaningful solution to this set of challenges starts with a separation between  those holding the data, and those collecting and/or using it. Enter a Data Trust: A piece of infrastructure to separate companies that collect and/or use (personal) data, from the custody of that data. The custodian is a non-profit, acting under the direction of a trust. This infrastructure allows data subjects to control under what conditions data about them is used. It places a fiduciary responsibility on that custodian (the trustee) to act in the best interest of the data subjects, as well as those impacted by the sharing of data under the custodian's control. 

In our design of a data trust we accept a number of real-world constraints and scope restrictions:
- We do not require any laws to be changed for our concept to be implemented. 
- Implementing a democratic governance process within a data trust is out of scope; therefore, the trust will have a rule-making process that is permanent.
- We do not believe short-cuts (for instance in the form of homomorphic encryption or federated learning) are advanced enough to provide true privacy. 
- We do not require human beings to have endless time and energy to spend on making decisions about their privacy. We call this the usability requirement.
- Any data trust needs to make explicit whether it prioritises prevention of loss, prevention of breech, or a guarantee of completeness. This is equivalent to the CAP theorem, for custody.
- We treat data as a set of claims, not a set of facts. A data set can contain contradictory claims.

To navigate these constraints in light of our vision of a data trust, we rely on a few key components, as discussed below.

### Better Consent through Proxies
To satisfy the Usability Problem, we propose to put consent proxies in charge of assessing the privacy risks of collecting and sharing data in specific contexts. Consent proxies would be trusted entities with domain specific knowledge charged with the creation of consent profiles that cover specific types of data in that domain. For instance, a trade union could function as a consent proxy for workers. Data subjects, in turn, can then adopt various consent profiles as their own. The use of a consent proxy makes it reasonably straightforward for data subjects to understand what they consent to and change their minds down the line. As well as defining and updating consent profiles, the consent proxy is tasked with negotiating the “Terms of Service” (or EULA) agreements between the Data Trust and Data Subjects. These agreements cover what data can be collected, stored and shared. It falls on the data custodian to ensure that data users adhere to the rules deriving from these consent profiles, through access control and periodic audits.

### Data Availability
Through a data trust, data that is currently enclosed by single platforms would be made more widely available. In principle, if company A can license specific data for a specific purpose and duration, then company B should be able to do so as well. In addition, data could also be made available to researchers or governments. Of course, the license attached to the data and specific access rights depend on the consent profiles adopted by the data subjects, negotiated in balance against general concerns regarding the impact of such data sharing on society at large.

### Data Portability
In order to ensure that individuals can move freely between data trusts, it is not enough to ensure that the data within the trust remains portable - we need to ensure that the granted consent (and the details of the rules) are portable as well. We do so by making consent portable. We conceive of a Consent Rules Engine and associated grammar that provides a cascading hierarchy of consent statements. Of course, true portability also requires data subjects have other data trusts to which they can move their data. We believe we can achieve a federated and portable ecosystem of data trusts by separating Protocol, Platform and License.

### Certification
In order to be able to trust the data trust, the data custodian should be required to obtain certification from an independent body. If it loses its certification, it should no longer be allowed to create data trusts - in any jurisdictions - and any existing data trusts should be dissolved (with data moved to other trusts). A healthy ecosystem of data trusts therefore also requires that no single data custodian ever holds a large enough share of the entire number of data trusts in a jurisdiction.


## What Comments Are We Asking For?

[Please have a look at the full document and leave any comments / ideas /questions.](https://docs.google.com/document/d/1e-PHibsPE-b4irLPzPmCJenlDTKf34EWljg0wF2Pizo/edit?usp=sharing) Thank you!


We are looking for general feedback and comments on the ideas presented in this RFC. In addition, there are still a number of open questions we would like your input on, specifically:
Incentives: Are the moral, technical and financial incentives strong enough for meaningful participation, without regulatory pressure?

**Liability:** Is the liability currently placed on the company/entity holding data reduced by offloading data to a trust?  Is it reduced enough?

**Governance:** Can we avoid voting? At the moment our design relies on low barriers of entry for the creation of data trusts, certification of data trusts, as well as low switching costs for data subjects as the main ways to ensure data subjects are sufficiently represented by the data custodian, without the need for democratic processes to govern control over data. Is this enough to prevent evil data trust empires from emerging? What other models could we envision? For context, the representative interests are:
- Trustees for subjects and impacted parties
- Data Subjects
- Impacted non-subjects

**Failure Modes?**
Can we develop a “FAIL-SAFE” Model for this trust, where it can “degrade gracefully”?
What happens when faith on data trust is eroded? 
How do we prevent one data trust to gain monopoly power? Are our ideas around portable data and consent sufficiently strong to mitigate this risk?
How do we ensure survival of data trust does not come at the expense of ethical data sharing?

**Consent over shared data:**
For simplicity, we have assumed a model of “joint account with sole survivorship”, which implies that shared data is wholly owned by each party. Is this enough? Or are new kinds of consent required to broker the relationship between data parties? If Kim messages Peter, can Kim then take a copy of those messages with them as they leave the trust? If the trust loses its certification, who has rights over those messages - if anyone?


