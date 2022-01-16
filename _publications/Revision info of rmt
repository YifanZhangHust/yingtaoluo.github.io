Manuscript Type: Regular


**************************
Reviewer: 1

Recommendation: Author Should Prepare A Major Revision For A Second Review

Comments:
The origination of the paper is good and it is easy for readers to understand the concept and contributions. The paper also has enough novelty. However, there are two main problems that needs to be explained by the authors.

At first, it is not easy for readers to understand how the synthetic rejected samples are generated in section 6.1. What does “ε features” mean? Could you please explain how we apply ε features in the generation process specifically? Why do you use the LR model to predict the default probabilities and why you can annotate the rejected samples as the approved samples? In my view, it sounds like making fake data and such data may not convince other people.

The second problem is about the testing dataset you used in the experiment on approval-rejection datasets and multi-policy datasets. If I understand it correctly, you used the fake data which you made up from the rejected samples as the testing datasets. Such kind of data has no ground-truth labels and the labels you used are predicted by LR models but it is still not the true labels. Why can you use these made-up labels to evaluate whether a model can well predict the default probability? It should not be used in testing datasets at all.

Additional Questions:
1.  Please explain how this manuscript advances this field of research and/or contributes something new to the literature.: Credit scoring models are usually constructed based on approved applications which will lead the missing-not-at-random selection bias in data.  Previous Multi-task learning approaches cannot optimize the task weights well in the feature distribution of rejected samples to decide how much information is shared between the two tasks. In order to solve this problem, the authors propose to learn the weights that control the information sharing from two tasks by a gating network based on rejection probabilities. With larger rejection probability, less reliable information can be learned in the default/non-default network and more information is shared from the rejection/approval network.

2. Is the manuscript technically sound? Please explain your answer under Public Comments below.: Partially

1. Which category describes this manuscript?: Research/Technology

2. How relevant is this manuscript to the readers of this periodical? Please explain your rating under Public Comments below.: Relevant

1. Are the title, abstract, and keywords appropriate? Please explain under Public Comments below.: Yes

2. Does the manuscript contain sufficient and appropriate references? Please explain under Public Comments below.: References are sufficient and appropriate

3. Does the introduction state the objectives of the manuscript in terms that encourage the reader to read on? Please explain your answer under Public Comments below.: Could be improved

4. How would you rate the organization of the manuscript? Is it focused? Is the length appropriate for the topic? Please explain under Public Comments below.: Could be improved

5. Please rate the readability of the manuscript. Explain your rating under Public Comments below.: Readable - but requires some effort to understand

6. Should the supplemental material be included? (Click on the Supplementary Files icon to view files): Does not apply, no supplementary files included

7. If yes to 6, should it be accepted: After revisions.  Please include explanation under Public Comments below.

Please rate the manuscript. Please explain your answer.: Fair


Reviewer: 3

Recommendation: Author Should Prepare A Minor Revision

Comments:

The strength of this paper:

The paper is well written and easy to follow. The motivation is clear and well supported by the experimental results. The idea investigated in this paper might inspire some other related tasks in information retrieval, data mining, or language processing. The proposed framework is flexible and can be extended into multiple rejection/approval strategies.

The weakness of this paper:

I would like to recommend the authors to clarify the challenges, novelty, and contribution in the proposed methods directly.

Since I don’t have a background in financial credit scoring, the definition of default/non-default classes confused me a lot. I would like to suggest the author give a more clear definition at the start of the introduction section. Considering the TKDE is a prestigious journal in general data mining, I suppose that the majority of our readers may not have background knowledge particularly. Hence, a clear definition or setup is potentially helpful for us to understand the problem.

The lemma.1 is quite strange to me since it seems that the author provides some proof of this lemma without supporting any theoretical main results in the following content. Maybe is more appropriate to name the section as intuition or motivation based on my understanding.

The last question is about the design of the learning architecture. In the proposed strategy, the information flow in the multi-task learning framework is from the task of rejection/approval classification to the default/non-default classification which can fit the data collection process and improve the performance. However, in the real-world scenario, should we consider inverting the information flow in the learning architecture? Like using the default/non-default prediction to filter the customers?

Additional Questions:
1.  Please explain how this manuscript advances this field of research and/or contributes something new to the literature.: This paper aims to solve the missing-not-at-random selection bias in financial credit scoring which is caused by the miss labels in rejected application samples. To address this problem, the authors propose a  novel multi-task learning methods which share the information from the rejection/approval task to improve the performance in the task of default/non-default classification. On the other hand, the authors also provide a theoretical analysis of the correlation between the two tasks. In the empirical studies, the experimental results fully support the proposed methods with detailed comparison, parameter studies, and visualisation.

2. Is the manuscript technically sound? Please explain your answer under Public Comments below.: Yes

1. Which category describes this manuscript?: Research/Technology

2. How relevant is this manuscript to the readers of this periodical? Please explain your rating under Public Comments below.: Very Relevant

1. Are the title, abstract, and keywords appropriate? Please explain under Public Comments below.: Yes

2. Does the manuscript contain sufficient and appropriate references? Please explain under Public Comments below.: References are sufficient and appropriate

3. Does the introduction state the objectives of the manuscript in terms that encourage the reader to read on? Please explain your answer under Public Comments below.: Yes

4. How would you rate the organization of the manuscript? Is it focused? Is the length appropriate for the topic? Please explain under Public Comments below.: Satisfactory

5. Please rate the readability of the manuscript. Explain your rating under Public Comments below.: Easy to read

6. Should the supplemental material be included? (Click on the Supplementary Files icon to view files): Does not apply, no supplementary files included

7. If yes to 6, should it be accepted: After revisions.  Please include explanation under Public Comments below.

Please rate the manuscript. Please explain your answer.: Excellent
