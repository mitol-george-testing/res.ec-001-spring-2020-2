---
content_type: page
parent_title: 'Module 3: Pedagogical Framework for Addressing Ethical Challenges '
parent_uid: 7eac5c4b-32a0-928c-eec9-3df651769dd0
title: Protected Attributes and "Fairness through Unawareness"
uid: 8d5b79a6-d48a-bb89-18c0-258cee333d68
---

{{< youtube "6EPDzvUNCd0" "https://ocw.mit.edu/resources/res-ec-001-exploring-fairness-in-machine-learning-for-international-development-spring-2020/module-three-framework/protected-attributes/protected-attributes-and-fairness-through-unawareness-exploring-fairness-in-machine-learning/6EPDzvUNCd0.vtt" >}}

[Protected Attributes and "Fairness through Unawareness" slides (PDF)]({{< baseurl >}}/resources/mitres_ec001s19_video6)

Learning Objectives
-------------------

*   Present some examples of disparate treatment and disparate impact in the media
*   Introduce protected attributes
*   Cover examples of laws that govern protected attributes
*   Introduce the concept of fairness through unawareness and challenges associated with applying it

Content
-------

### Disparate treatment vs disparate impact

Disparate treatment is when you are disproportionately favoring a particular protected class by intentionally including variables tied to protected attributes. Disparate impact is when you are disproportionately favoring a particular group unintentionally.

### Examples of relevant unfairness

*   [Amazon example](https://fortune.com/2018/10/10/amazon-ai-recruitment-bias-women-sexist/): Amazon implemented a machine learning algorithm to screen resumes for hiring. Despite having gender as a predicted attribute, the algorithm discriminated against women. 
*   [Recidivism example](https://www.technologyreview.com/s/612775/algorithms-criminal-justice-ai/): Machine learning is being used in the criminal justice system to look at recidivism, the risk of a criminal reoffending after being released. This system has been shown to be potentially discriminatory across race and gender. 
*   [Facebook example](https://www.nytimes.com/2019/03/28/us/politics/facebook-housing-discrimination.html): Facebook was found to be discriminating by allowing advertisers to restrict who could see ads based on characteristics like race, religion, and national origin. 

### Protected attributes

Protected attributes are features that may not be used as the basis for decisions. Protected attributes could be chosen because of legal mandates or because of organizational values. Some common protected attributes include race, religion, national origin, gender, marital status, age, and socioeconomic status.

### Examples of conventions and laws in the US

1.  Penalties for discriminating in housing (US Fair Housing Act)
2.  Hiring (the collection of laws also known as Federal Equal Employment Opportunity – Civil Rights Act Title VII 1964, EPA 1963, ADEA 1967, ADA 1990, Rehabilitation Act 1973, Civil Rights Act 1991, GINA 2008)
3.  The most recent of these (ECOA) requires firms to test algorithms for unfair outcomes and has penalties for failures in testing.

### Examples of conventions and laws outside the US

1.  Convention against discrimination in education (UNESCO, 1960)
2.  Convention on the Elimination of All Forms of Racial Discrimination (UN General Assembly, 1965)
3.  Convention on the Elimination of All Forms of Discrimination against Women (UN General Assembly, 1979)
4.  Convention on the Rights of Persons with Disabilities (UN 2006)
5.  Many countries have codified protected attributes in their constitution.

### Fairness at the training set

When implementing a machine learning algorithm, you start by collecting data. Data contains outcome variables as well as predictor variables. The complete dataset is split into a training set where you run your model and a test set where you test your model to determine model performance. Implementing fairness starts with the training set. The training set can carry the biases of the people labeling data. In the case of resumes, if you have a set of graders and those graders have biases, those biases could be reflected in how the data is labeled. Bad training data will lead to a bad prediction. The training data may not be representative of all groups (for example, gender). Past data may not predict current events. Risks from training data include biased sampling, small sample sizes for certain subgroups, hidden correlations, the possibility that the data may contain protected variables, and a large degree of noise.

### Fairness through unawareness

Fairness through unawareness assumes that if we are unaware of protected attributes while making decisions, our decisions will be fair. This approach has been shown to not be effective in many cases. Protected variables could be correlated with other variables in the data. For example, race or religion may be linked to a city or neighborhood in a city.

Discussion Questions
--------------------

*   What are protected attributes?
*   Do you think the current list of protected attributes is exhaustive? Are there others you might add?
*   What is “fairness through unawareness”?
*   What are some problems in the Amazon approach?
*   What might be some protected attributes in the recidivism example?
*   What are some risks to an organization in choosing “unawareness”?

References
----------

Abdi, H. "The Kendall Rank Correlation Coefficient." _Encyclopedia of Measurement and Statistics_. Sage, Thousand Oaks, CA (2007).

Agrawal, Ajay, Joshua Gans, and Avi Goldfarb. _Prediction Machines: The Simple Economics of Artificial Intelligence_. Harvard Business Press, 2018.

Ajunwa, Ifeoma. "The Paradox of Automation as Anti-Bias Intervention." \[_Forthcoming in Cardozo Law Review (2020)_.\] March 10 (2020): 2016.

Angst, Corey M., and Ritu Agarwal. "Adoption of electronic health records in the presence of privacy concerns: The elaboration likelihood model and individual persuasion." _MIS Quarterly_ 33.2 (2009): 339–370.

Angst, Corey M. "Protect my privacy or support the common-good? Ethical questions about electronic health information exchanges." _Journal of Business Ethics_ 90.2 (2009): 169–178.

Apfelbaum, Evan P., et al. "In blind pursuit of racial equality?" _Psychological Science_ 21.11 (2010): 1587–1592.

Ashcraft, Catherine, Brad McLain, and Elizabeth Eger. _Women in Tech: The Fact_s. National Center for Women & Technology (NCWIT), 2016.

Contributions
-------------

Content presented by Mike Teodorescu (MIT/Boston College).

This content was developed in collaboration with Lily Morse and Gerald Kane (Boston College) and Yazeed Awwad (MIT).