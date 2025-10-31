# Predicting news post performance with a Random Forest model

## Objective
Develop a simple machine learning model to predict the perfomance (engagement) of news post using only information available before publication, such as text length, sentiment and topic

## Methodology
Using a small dataset of journalistic posts labeled by topic, text length, and sentiment score
<img width="766" height="181" alt="image" src="https://github.com/user-attachments/assets/ae3c2878-da09-455d-ba97-379c0218b7f6" />

Create an engagement column based on the business rule: likes = weight 1, shares = weight 2 and comments weight = 3
<img width="653" height="285" alt="image" src="https://github.com/user-attachments/assets/ccccccce-bc84-48fd-ae3a-d6ab6e5457ea" />

Tested multiple label strategies for the z-score of engagement
<img width="826" height="460" alt="image" src="https://github.com/user-attachments/assets/a58f934e-fc97-491a-8743-3bd141302119" />

Trained a Random Forest model using the features Word_Count, Sentiment and Topic
<img width="583" height="145" alt="image" src="https://github.com/user-attachments/assets/b62f00e4-57a3-41b8-8159-08d557569935" />

## Key Findings
Form and tone (Word_Count and Sentiment) explain most of the variation in engagement

Topic has influence, but to a lesser extent. This suggest that writing style impacts more than subject matter
<img width="414" height="419" alt="image" src="https://github.com/user-attachments/assets/d163d7b9-301a-49b1-ba42-ba9f36e155e5" />

## Limitations
Limited text features. The model relied mostly on two variables

No temporal or platform context (posting time, channel, headline style, etc)

## Learnings
Testing different target definitions (Z-score) is essential.

For the next steps, testing regression and lightweight transformer models for semantic interpretation
