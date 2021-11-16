---
content_type: page
parent_title: 'Module 3: Pedagogical Framework for Addressing Ethical Challenges '
parent_uid: 7eac5c4b-32a0-928c-eec9-3df651769dd0
title: Fairness Criteria
uid: 1c0498f4-4dca-ffcb-365a-4a06ad7bbeb4
---

{{< youtube "euwc0va-7Vo" "https://ocw.mit.edu/resources/res-ec-001-exploring-fairness-in-machine-learning-for-international-development-spring-2020/module-three-framework/fairness-criteria/fairness-criteria-exploring-fairness-in-machine-learning/euwc0va-7Vo.vtt" >}}

[Fairness Criteria slides (PDF - 1.5MB)]({{< baseurl >}}/resources/mitres_ec001s19_video5)

Learning Objectives
-------------------

*   Present the confusion matrix, including definitions for true negatives, true positives, false negatives, and false positives.
*   Discuss how to choose between different fairness criteria including demographic parity, equalized odds, and equalized opportunity.

Content
-------

### Confusion matrix

In the case of a binary classification (for example, whether or not to hire someone), you can categorize values in four categories. TP = true positive (correctly classified as positive). TN = true negative (correctly classified as negative). FP = false positive (incorrectly classified as positive). FN = false negative (incorrectly classified as negative).

![Four square chart of actual vs predicted results.](BASEURL_PLACEHOLDER/resources/res-ec-001-fairness-criteria)

### Demographic parity

The outcome is independent of the protected attribute. For example, the probability of being hired is independent of gender. Demographic parity almost always cannot be implemented if individuals are members of multiple protected groups because you may not be able to impose the equal probabilities across all groups. Demographic parity can also be fair at a group level, but unfair at an individual level. For example, if qualifications are different across a protected attribute, imposing demographic parity may mean someone who is less qualified may get hired. Therefore, if a large number of unqualified male applicants is added to the applicant pool, the hiring of qualified female applicants will go down.

### Equalized odds

Equalizing the odds means matching the true positive rates and false positive rates for different values of the protected attribute. This means that we are only enforcing equality among individuals who reach similar outcomes. This algorithm is more challenging to implement, but achieves one of the highest levels of algorithmic fairness. For example, the probability for a qualified applicant being hired and the probability of an unqualified applicant not being hired should be the same across all protected attributes. As compared to demographic parity, if a large number of unqualified male applicants apply for the job, the hiring of qualified female applicants in other protected groups is not affected.

### Equalized opportunity

Equalized opportunity means matching the true positive rates for different values of the protected attribute. This is a less interventionist approach of equalizing the odds and may be more achievable. In the example of hiring, for qualified applicants, the algorithm would work exactly as the equalized odds algorithm. For unqualified applicants, the rates of not hiring would not be same across different values of the protected attributes. For example, unqualified men would not necessarily have the same rate of not being hired as unqualified women.

Discussion Questions:
---------------------

*   What is "demographic parity"? What is an example where you would want to use it?
*   How might the overall accuracy of your algorithm change when applying these different fairness metrics?
*   How do equalized odds and equalized opportunity differ? What is an example of where you would want to use one but not the other?

References
----------

Hardt, Moritz, Eric Price, and Nati Srebro. "Equality of opportunity in supervised learning." _Advances in Neural Information Processing Systems_. 2016.

Kilbertus, Niki, et al. "Avoiding discrimination through causal reasoning." _Advances in Neural Information Processing Systems_. 2017.

Wadsworth, Christina, Francesca Vera, and Chris Piech. "[Achieving fairness through adversarial learning: an application to recidivism prediction](https://arxiv.org/abs/1807.00199)." arXiv preprint arXiv:1807.00199 (2018).

Pleiss, Geoff, et al. "On fairness and calibration." _Advances in Neural Information Processing Systems._ 2017.

Verma, Sahil, and Julia Rubin. "Fairness definitions explained." _2018 IEEE/ACM International Workshop on Software Fairness (FairWare)_. IEEE, 2018.

Contributions
-------------

Content presented by Mike Teodorescu (MIT/Boston College).

This content was developed in collaboration with Lily Morse and Gerald Kane (Boston College) and Yazeed Awwad (MIT).