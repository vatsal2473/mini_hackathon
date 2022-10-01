## Classification of stance and premise in tweets about health mandates related to COVID-19 (in English)

Users are actively sharing their views on various issues on social networks. Nowadays, these issues are often related to the COVID-19 pandemic. For example, users express their attitude towards a quarantine and wearing masks in public places. Some statements are reasoned by arguments, other statements are just emotional claims. Automated approaches for detecting people's stances towards health orders related to COVID-19, using Twitter posts, can help to estimate the level of cooperation with the mandates. In this task we focus on argument mining (or argumentation mining) for extracting arguments from COVID-related tweets. According to argumentation theory, an argument must include a claim containing a stance towards some topic or object, and at least one premise/argument (“favor” or “against”) of this stance.

 

Participants will be provided with labeled training set containing texts from Twitter about three health mandates related to COVID-19 pandemic:

* Face Masks
* Stay At Home Orders
* School closures


**Data**

We will provide participants with manually labeled tweets for training, validation and testing. The train set for stance detection subtask is based on a COVID-19 stance detection dataset (Glandt et al., 2021).

* Train: 2756 tweets
* Validation: 600 tweets
* Test: 800 tweets
 

### Subtask 2a. Stance Detection

The designed system for this subtask should be able to determine the point of view (stance) of the text’s author in relation to the given claim (e.g., wearing a face mask). The tweets in the training dataset are manually annotated for stance according to three categories: in-favor, against, and neither. Given a tweet, participants of this subtask will be required to submit three classes annotations:

* **FAVOR** – positive stance
* **AGAINST** – negative stance
* **NEITHER** – neutral/unclear/irrelevant stance 
 

### Subtask 2b. Premise Classification

The second subtask is to predict whether at least one premise/argument is mentioned in the text. A given tweet is considered as having a premise if it contains a statement that can be used as an argument in a discussion. For instance, the annotator could use it to convince an opponent about the given claim.

Given a tweet, participants of this subtask will be required to submit only the binary annotations:

* **1** – tweet contains a premise (argument)
* **0** – tweet doesn't contain a premise (argument)

**Evaluation Metrics :**

The main performance metric in each of the two subtasks are F1𝑠𝑡𝑎𝑛𝑐𝑒 and F1𝑝𝑟𝑒𝑚𝑖𝑠𝑒 scores respectively,

which are calculated according to the following formula: 

![Screen-Shot-2022-04-01-at-10 26 16-AM](https://user-images.githubusercontent.com/78549124/187269424-0dfc4ba7-009e-462b-985c-064632f98f6d.jpg)

where:
𝐶 = {“face masks”,”stay at home orders”,”school closures”},
𝑛 is the size of 𝐶,
𝐹1𝑟𝑒𝑙 score is macro 𝐹1-score averaged over first two relevance classes (the class “NEITHER” is excluded).

![Screenshot_20220829_235649](https://user-images.githubusercontent.com/78549124/187272101-846183ec-e3db-419b-8744-91c3e751f49f.png)


