---
content_type: page
parent_title: 'Module 2: Examples of Ethical Challenges in Machine Learning'
parent_uid: e5c9ce69-6e54-9096-c82b-62631a8b712b
title: Solar Lighting Example
uid: 81e0b58f-33da-44c7-27c4-e0d948632623
---

{{< youtube "neG4seg61VU" "https://ocw.mit.edu/resources/res-ec-001-exploring-fairness-in-machine-learning-for-international-development-spring-2020/module-two-ethical-challenges/solar-lighting-example/solar-lighting-example-exploring-fairness-in-machine-learning/neG4seg61VU.vtt" >}}

[Solar Lighting Example slides (PDF)]({{< baseurl >}}/resources/mitres_ec001s19_video4)

Learning Objectives
-------------------

*   Present a case study in which a government/non-governmental organization/social enterprise may want to incorporate machine learning.
*   Discuss pros and cons of implementing ML-based solutions.
*   Highlight important interactions between the ML implementer and an organization.
*   Raise examples of how implementing ML without paying attention to fairness could have negative effects.
*   Discover how implementation of algorithms is not objective.

Content
-------

We will start by presenting a case study on the evolution of machine learning in the solar lighting industry.

### Introduction

In this case study, we will be taking the role of a chief technology officer of a social enterprise that provides solar lighting products in East Africa. The mission of the company is to provide affordable lighting solutions to people living in poverty and the company started by providing high-quality, inexpensive solar lights that were replacements for kerosene lanterns.

Over time, the company has grown and increased its product offerings to include larger solar home systems, and along the way has implemented pay-as-you-go models, so that households can afford to purchase these larger systems. The way the pay-as-you-go model works is that the company provides the solar lighting infrastructure as a loaned asset to individuals and is paid back over time through mobile money payments until the full value of the asset is recovered.

The company has been meticulous about keeping records from transactions from their userbase and as a result, has access to both demographic information and payment history from its clients. The information from the users includes age, gender, occupation, location, and household income. As the company looks at expanding its social impact, they realize that this data can be analyzed to determine a credit worthiness metric for their customers. Additionally, they could provide this information to banks or microfinance institutions so that they can give loans to their client base.

### In-house vs external implementation

Machine learning is a powerful tool that you can use to implement this credit scoring metric, however the company does not have data scientists or machine learning experts within their team that can implement this solution. They also do not know how accurate or powerful the algorithm that they develop could be, so do not want to spend the resources to build a full team and opt to run a small pilot with some users in Uganda. As a resourceful company with engineering staff, they could either train some of the engineers to implement a machine learning solution using off-the-shelf solutions to credit scoring or work with a third-party company to implement the solution.

To consider the pros and cons of each approach, it is important to consider the perspectives from both a machine learning implementer as well as the organizations to understand thoughts and complexities that go into developing a solution. Doing it in-house without a trained data scientist would likely involve the implementation of a black box solution. While someone with no background in machine learning could get a solution up and running fairly quickly, there are several nuances in design that may get overlooked. Allowing a third-party consultant to implement the solution would solve many of these issues, though the organization may lack the in-house capabilities both to understand how the model is being implemented and maintain it moving forward. Additionally, this approach may be expensive.

### Ethical challenges in implementation

First, historical data that certain groups of people may have different default rates than others. For example, women may have a lower default rate than men and the organization will have to decide how to address the issue (they will likely want to be fair and gender-blind in loan determination). To implement fairness, a naïve implementer may first try to use fairness through unawareness, which means they simply hide gender information when building the models. Depending on correlations within the data and how relevant gender is to default rates, the models could still predict gender and use that in the model.

Second, since data shows a difference in default rates, someone has to actively decide how to correct for that. In the case of loans, different approaches to implement fairness may have a trade-off with the accuracy of the algorithms as well. Third, the type of algorithms the implementer uses could have trade-offs as well. Some algorithms may be faster at the cost of accuracy, others may be more accurate at the cost of explainability or understandability.

### Important takeaway points

First, implementing a machine learning algorithm is not an objective process. In your implementation, you are both designing a technology and making decisions, both of which introduce your biases into the system. To think that outcomes from a computer are objective is a fantasy.

Second, open communication between you and the implementer on your values as an organization and decisions that they are making in implementation are critical.

Third, you need a way to audit your data and your algorithms if you want to have a fair system.

### Challenges with scaling

Let’s move on assuming you were able to work with a consultant to build a satisfactory solution to your algorithm and you are able to demonstrate significant success with your pilot in western Uganda. You now want to scale your model to other parts of Uganda and East Africa. At this point, it is important to pay attention to the representativeness of your data. Are there large differences between the types of users you have in Western Uganda and Eastern Uganda? Are there large differences between the types of users you have in Uganda and Tanzania? You need to make sure that you are collecting representative data as you scale your solution which involves significant testing and auditing.

Additionally, you want to make sure that changes within your population do not suddenly affect your results. For example, if a kerosene tax were imposed by the government, would your model no longer be accurate? How could you build in support within your organization to make sure that you can react to change?

Discussion Questions
--------------------

*   If you were to collect data on users when building a credit algorithm, which data would you collect and which data would you not collect?
*   Would you implement the algorithm in-house or outsource it to an implementing firm?
    *   What are the pros and cons of each option?
*   What are some other ways that the organization could apply machine learning to their business?

References
----------

"[Meet Pulse – BBOXX’s pioneering predictive management platform for distributed energy businesses](https://www.bboxx.com/news/launch-of-bboxx-pulse/)." _Bboxx_, 2019.

Popescu, Adam. "[AI Helps Africa Bypass the Grid](https://www.bloomberg.com/news/articles/2018-06-11/ai-helps-africa-bypass-the-grid)." _Bloomberg_, 11 June 2018. 

Contributions
-------------

Content created and presented by Amit Gandhi (MIT).