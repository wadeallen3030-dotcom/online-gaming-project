# online gaming project

This is a practice project I made with the dataset "Predict Online Gaming Behavior Dataset" downloaded from Kaggle. I also used Chatgpt to generate some real-world questions to enhance the overall practice purpose. The questions can be categorized into the followings:

## 1. Player Behavior Analysis
   -	What is the average and median playtime per player?
   -	How does playtime differ by gender or age group?
   -	Do younger players tend to have more sessions but shorter playtime?
   -	What percentage of players are highly active (top 20% by playtime)?
  
## 2. Retention & Engagement Analysis
   -  Is there a relationship between session count and retention indicators?
   -  What % of players have never spent money?
   -  Do paying players have higher session frequency than non-paying players?
   -  What behavioral patterns differentiate retained vs churned players?

## 3. Analytical Thinking
   -  Based on behavior, which players are most likely to spend?
   -  If marketing targets the top 30% engaged non-paying users, how many users is that?

I present most of the qeutions in 3 dashboards, each could address one of the questions along with some findings, and I'll breakdown my work process.

<img width="1077" height="584" alt="general dashboard" src="https://github.com/user-attachments/assets/c9818d55-c79a-43fe-868f-8d8c2a9dbb51" />


## Player Behavior Analysis Progress breakdown

<img width="1147" height="583" alt="image" src="https://github.com/user-attachments/assets/4940c3d7-28fd-4174-a1c9-ca801d0128d8" />


Question 1: What is the average and median playtime per player?
I used formulas (=AVERAGE), (=MEDIAN) to calculate the nubmers.
<img width="549" height="127" alt="image" src="https://github.com/user-attachments/assets/4e4805ac-6c1f-4bd8-b7a1-137f520acfa5" />


Question 2: How does playtime differ by gender or age group?
I used pivot table to find the differenec. I also had to create a age group within the pivot table to avoid too many rows.
<img width="878" height="139" alt="image" src="https://github.com/user-attachments/assets/d943179f-8926-47d7-999d-29f9d00e2300" />

Question 3: Do younger players tend to have more sessions but shorter playtime?
I used pivot table to find the trend. Judging by the result, younger players do not tend to hav more sessions or shorter paytime.
<img width="752" height="125" alt="image" src="https://github.com/user-attachments/assets/1f02bb38-9752-4f9e-bb07-2cac00fcb693" />

Question 4: What percentage of players are highly active (top 20% by playtime)?
First I had to define highly active players. To do that I have to find the top 20% thresold first, and I used PERCENTILE.INC(playtimehours, 0.8) to find out the number, then use IF formula to categorized players into "highly active" and "standard" groups, then put them into pivot tbale to have both the count and percentage.
<img width="750" height="79" alt="image" src="https://github.com/user-attachments/assets/964369fc-be9e-4205-828e-4da3167e7d9b" />


## Retention & Engagement Analysis

Question 1: Is there a relationship between session count and retention indicators?
I used Engagementlevel as retention indicators, and I put it along with session count to pivot table and then pivot chart to find the result. It shows that players who have higher engagement level do have more play session counts which indicates a possitive relation.
<img width="819" height="418" alt="image" src="https://github.com/user-attachments/assets/ce9d7ac4-2f19-464f-8de1-6d8e8cde6c45" />

Question 2: What % of players have never spent money?
I used the Ingamepurdhase made data along with player ID count for a pivot chart.
<img width="467" height="265" alt="image" src="https://github.com/user-attachments/assets/ed49aad1-2ee1-4709-962e-3f0cbcec17c7" />

Question 3: Do paying players have higher session frequency than non-paying players?
I used IF formulas to change Ingamepurdhase data into "YES" and "NO" label for better visibility, then use that along average sessions per week to build a pivot chart. The result shows that spending players do have bit more play sessions than non-paying players. but the different is neglectable. 

<img width="294" height="283" alt="image" src="https://github.com/user-attachments/assets/9e0bed2f-4f99-4f00-9884-52160ba49efb" />

Question 4: What behavioral patterns differentiate retained vs churned players?
After analyzing a few different combination, it seems that churned players tend to have lower levels comparing to retained players.
<img width="547" height="350" alt="image" src="https://github.com/user-attachments/assets/18ba39f3-2ef7-4dfe-9238-dccaaba62051" />


## Analytical Thinking

Question 1: Based on behavior, which players are most likely to spend?
I comebined engagement level, game difficulty and count people of in-game purchase made, it turns out that playres with median engagement level who are playing easy mode is more likely to spendi comparing to other groups.

<img width="752" height="452" alt="image" src="https://github.com/user-attachments/assets/c4dd30db-6478-4ef1-bbc2-3195468a0f64" />

Question 2: If marketing targets the top 30% engaged non-paying users, how many users is that?
This one's pretty easy, we just need to filter high engagement players without purchase made with pivot table, then take that number and times 30% to find th result.
<img width="655" height="160" alt="image" src="https://github.com/user-attachments/assets/182fdcba-ae57-49f4-8676-9601c1e2e5e9" />


# Conclusion
1. The average spending player base, average play time among males and females are surprisingly close, indicating that gender is not the main reason for purchase decision.
2. We did find out that players with mid level engagement and play easy mode are more likely to spend. We could suggest the Dev team to focus more of the in-game content at this part to drive revenue.
