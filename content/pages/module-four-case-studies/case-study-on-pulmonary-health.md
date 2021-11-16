---
content_type: page
parent_title: 'Module 4: Case Studies with Data '
parent_uid: cce773cc-98d0-45b1-b181-83c340d2d168
title: Case Study on Pulmonary Health
uid: e927237f-0504-d17b-16db-1e7afce2a68e
---

{{< youtube "zrB6pocJSI8" "https://ocw.mit.edu/resources/res-ec-001-exploring-fairness-in-machine-learning-for-international-development-spring-2020/module-four-case-studies/case-study-on-pulmonary-health/pulmonary-health-case-study-bias-exploration-exploring-fairness-in-machine-learning/zrB6pocJSI8.vtt" >}}

[Case Study on Pulmonary Health slides (PDF - 1.2MB)]({{< baseurl >}}/resources/mitres_ec001s19_video8)

Learning Objectives
-------------------

*   Present a case study on pulmonary health diagnostics.
*   Explore the influence of representative data on accuracy.

Content
-------

### Introduction

Pulmonary diseases, including asthma, COPD, allergic rhinitis, and others can have significant detrimental health impacts if undetected. In remote areas with limited access to healthcare, they can often go undiagnosed and untreated. The motivation for this work was to develop a screening tool for community healthcare workers to determine if patients who were presenting symptoms of pulmonary disease actually have pulmonary disease.

To develop the tool, data was collected from 303 patients who sought medical care at health clinics between 2015 and 2018 in Pune, India. Patient data was collected at health clinics from two exams, a mobile diagnostic kit developed by Dr. Fletcher’s group and a set of measurements from a Pulmonary Function Test lab by the research team, and health diagnoses were performed by medical staff with a focus on asthma, allergic rhinitis, and COPD.

### Study design

This exploration of representative sampling on accuracy was conducted across two protected variables: gender and income. For income considerations, patients were categorized as either low-income or high-income. The overall approach to the bias study was to divide the dataset into a larger training data superset and a test dataset. A logistic regression model with L2 regularization was used to make predictions on disease.

To train the model, training data subsets were randomly sampled from the superset that intentionally introduced imbalances along protected variables. For example, with regards to income, training data subsets ranged from 50% high-income to 50% low-income and 87.5% high-income to 12.5% low-income. To account for stochastic error, this process was run 1000 times for each test. The area under the curve of the receiver operating characteristic curve was used as the metric for accuracy.

### Results

The results for predictive accuracy for AR, Asthma, and COPD are shown below. The data shows no significant decrease in algorithm accuracy as gender imbalances are introduced in the data. It is important to note that protected variables do not necessarily affect outcome variables and that lack of representativeness may not always introduce bias or unfairness into models.

![Line graph of COPD gender AUC results](BASEURL_PLACEHOLDER/resources/res-ec-001-pulmonary1) ![Line graph of ASTHMA gender AUC results](BASEURL_PLACEHOLDER/resources/res-ec-001-pulmonary2)

![Line graph of AR gender AUC results](BASEURL_PLACEHOLDER/resources/res-ec-001-pulmonary3)

In our dataset, we found that smoking heavily correlated with gender. 55% of men reported that they were non-smokers, whereas 100% of women reported that they were non-smokers. As a result, the population of women was more homogenous, allowing for higher predictive accuracy.

The results for predictive accuracy for AR, Asthma, and COPD are shown below. Again, we see little difference in accuracy as we change representativeness within the sample. COPD is the most sensitive to socio-economic status with a 4% difference in model accuracy for high-income and low-income populations. Asthma and allergic rhinitis show no difference in performance.

![Line graph of COPD socioeconomic AUC results](BASEURL_PLACEHOLDER/resources/res-ec-001-pulmonary4) ![Line graph of ASTHMA socioeconomic AUC results](BASEURL_PLACEHOLDER/resources/res-ec-001-pulmonary5)

![Line graph of AR socioeconomic AUC results](BASEURL_PLACEHOLDER/resources/res-ec-001-pulmonary6)

Contributions
-------------

Content presented by Amit Gandhi (MIT).

The research and content for this module was conducted by Rich Fletcher and Olasubomi Olubeko (MIT) in collaboration with the Chest Research Foundation. Additional funding for the project was provided by NSF and the Vodafone Americas Foundation.