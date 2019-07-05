---
layout: post
title:  "Data Portability, Federation And Portable Consent"
date: 2019-07-03 14:08:11 +0200
categories: privacy consent
description: In order to have real choice online, we need portable data and consent. We need separate platforms, protocols and licenses, such that each represents a check or balance on the others.
image: data.jpg 
authors:
 - josh
 - anouk
---

Online consent is broken. The enclosure of user data by social media platforms and services have resulted in power imbalances that undermine any meaningful notion of consent. Our ability to freely choose how and when we share our data breaks down when the 'choice' is between surrendering data about ourselves or social exclusion. A different reality is possible: one where we can leave a social media platform, and take our social graph and data with us; one in which we can vote with our feet, and thereby change the power dynamic between us and the platforms we rely on for our everyday communication.

The internet itself was conceived of as an “open” platform - where open, in this case, means that the legal entities, the technical solutions used, and the future classes of content, can all be evolved independent of each other. This combines portability and federation. Portability refers to the idea that any single website or network-connected device can be moved between existing entities. Federation means that new websites and devices can be connected without requiring the participation of existing entities. Taken together, the combination of portability and federation can provide a robust set of protections for individual and societal freedoms.

Under the General Data Protection Regulation that came into effect in Europe last year, individuals gained a right to data portability. We can now decide to leave Facebook and take our personal data with us to another service. In theory, we are no longer beholden to one social media platform or banking app and are free to break out of the walled gardens that have held us hostage. In reality, we rarely exercise our right to data portability. For starters, it's hard to actually obtain the data about us. Additionally, data derived from one service is often not directly usable for another. 

What mechanisms and infrastructure need to be in place to realize true portability and federation?


## The separation of powers: protocol, platform and license

We can divide the problem of providing portability into three segments: Protocol, Platform, and License. We argue that data portability and federation requires each of these segments to be created independent of the others, such that no single segment can ever prescribe rules to the remaining two.

**Protocol** describes the relationship between data and the set of explicit consents that have been granted on that data. Take the git protocol as an example, which describes the history of changes to a data set and the authors of those changes. 

**Platform** is envisioned as a server environment that supports real-time API-driven access to data sets, mediated by a rules engine that conforms to the Protocol. This includes a set of read and write clients, as well as standalone policy engines that enforce pre-collection permissions and post-read usage and summarization consent. All of the components of the platform are designed to allow robust audit capabilities, and a tamper-proof activity log. 

To return to the git example, this open protocol works with various platforms, like GitHub and GitLab. If users of one of these platforms stop trusting in its governance, they can easily take their code base to a different platform. In the extreme case, they can run a platform themselves.

**License** provides a permanently-attached set of limits on usage and derived work, and functions exactly the same as copy-left or permissive licensing in the open source world. Note that extended permutations of the copy-left principles (including licenses that explicitly prohibit commercial activity) are likely to emerge in this space. Additionally, licenses and other legal frameworks are the only portion of a data trust structure that remains ATTACHED to the data after it is exported; thus, they are critical to protecting the integrity of the consent(s) during migrations.

## Portable Consent: An unavoidable complexity

When transferring data between services, or organisations, we need to be able to ensure that the privacy statements attached to the data are upheld. In other words, if data is moved from one social media to another, a user should be able to trust that the privacy settings agreed to on the first platform, equally apply on the second. This means that the mechanisms for managing consent need to exist at the protocol and license layer, decoupled from the platform. 

In order for protocols to provide meaningful portability guarantees, there must be at least one platform available that implements this protocol (such as GIT for the git protocol, httpd for the HTTP protocol) and that platform must be a) operated by at least two different entities, and b) be relatively simple for an additional entity to operate. Any data trust operator could swap out the underlying platform without breaking portability, provided the same underlying protocol was supported.

Moreover, the entity that defines and evolves the protocol should ideally be separate from any of the entities that operate these platforms - much in the same way the W3C is separate from any specific browser.

## Conclusion
Each of the three aspects of portability represents a check or balance on the others. Licenses and protocols can both be abused to tightly couple data to a specific platform; similarly, protocols can be structured in a way to limit the potential licenses with which they could be used. Users and their consent proxies should remain free to select the license of their choice, unconstrained by platform or protocol limitations.