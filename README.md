<img width="1501" alt="Screen Shot 2024-04-02 at 3 22 32 PM" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/108fb197-e8eb-4339-b2c8-3d841ba0f807">

# Website User Behavior Analysis
Taiwan ICDF Bamboo Industrialization Project in Guatemala is dedicated to fostering sustainable bamboo industries throughout Guatemala. Our mission involves offering comprehensive technical assistance to industry participants, empowering them with the knowledge and skills needed to thrive in this sector.

To achieve our goals, we use the Bamboo Industrialization Project website as a platform for introducing and promoting our projects. Through this online platform, we aim to raise awareness about the project, its objectives, and the opportunities it presents for individuals and communities. Moreover, we seek to encourage greater participation in the bamboo industry by extending invitations to interested stakeholders to join our cause and contribute to its success.

## Problem Description
We are facing many challenges in terms of brand awareness and increasing the number of participants from the existing bamboo industry. Our main goal is to spread the word about the economic potential and environmental benefits of bamboo, the technical support we can offer, and encourage more individuals to be part of the growing bamboo economy in Guatemala. 

By analyzing website user behavior, we aim to gain insights into our website visitors and their interactions with our platform. With this understanding, we can offer tailored suggestions to enhance our website content and improve user experience.

## Exploratory Data Analysis
The dataset covers the period from January 15th, 2024 to March 15th, 2024, totaling 8743 activity records. After thorough organization and sorting, we've condensed this information into 804 user data.

#### Table 1: User data
![user data dataframe](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/2f27c56d-0a97-4d83-bad4-812e3b7a56e0)

#### Table 2: User data summary
![user data summary](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/55a4854b-81fc-44b4-a193-f5c7f8a8fd89)

#### Figure 1: Event count distribution
<img width="800" alt="30" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/60bfd2fb-2058-497f-9629-1327346ea23c">

#### Figure 2: User engagement distribution
<img width="800" alt="30" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/d6886ab0-8d3e-4083-a091-f385a3f2d94c">

#### Figure 3: Geographical information pie chart
<img width="500" alt="30" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/33913a9b-e4df-4cbe-bef8-f2c4678c7470">
<img width="230" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8aee6717-0a5e-416f-a1bd-b438cbb165e9">

#### Figure 4: Correlation Matrix
<img width="800" alt="50" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/71435e82-ee69-4962-a084-3e6824d0b130">

## Feature Engineering

#### Table 3: Standardizing data
![standardized user data](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/26ff864f-2d60-4622-b874-a7b4f3477905)

#### Figure 5: Principal components composition
<img width="500" alt="30" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/f2d1ce05-3667-4e2e-b5a1-297e3200ddbb">

#### Figure 6: Selecting the number of principal components
<img width="500" alt="30" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/45ce3a76-f69e-4ede-b7d4-c80ca0641e5a">
<img width="350" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/378b1a56-da9c-4d9b-8e9f-73ecd02e3a94">

#### Table 4: Transforming data
<img width="900" alt="pca" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/15f07d40-a405-4351-802f-f97f9e852c95">

## Model Building and Evaluation

#### The elbow method
![elbow method](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/cee0f6f1-300a-4370-bea5-02e751ade0f2)

#### The silhouette method
![silhouette method](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/b77695f7-c497-42df-a464-0445bb1f2cae)

## Results
#### User cluster pie chart
<img width="413" alt="Screen Shot 2024-04-03 at 11 14 09 AM" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/d8108b8f-eab3-46cf-baf3-77dc122190ac">

#### Cluster scatter plot
![cluster scatter plot](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/873aa75a-023b-4a65-9c90-e9ed2d7def86)
![2](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/f79771f1-6d3c-4d6b-85cb-744d04a9a8a0)
![3](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8fa51316-ad54-41ef-a800-0d7261fb61b9)
![4 11 42 59 AM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/0935f478-7555-46f8-95f1-4aa0c8ff2c86)
![5](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/eca21c41-c959-424b-9e31-4c6d4c37e806)
![6 11 42 59 AM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/3672127f-4b2c-40de-9521-31acf19a9976)
![7 11 42 59 AM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/a981793c-8af0-401a-bcaa-23b2ffaa51e7)
![8](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/389ccfc5-19a6-4370-b360-20fc5d6cfa1f)

## Exploration of clusters
#### Cluster summary
![cluster summary](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/d19595d9-ba23-4fda-b6e8-9bb9e8ddb227)

#### Figure ..: data per cluster
![1](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/78fa7ca9-ff6f-4727-8ebb-198752c629d0)
![2 12 30 00 PM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/de2291bc-89ee-4151-998b-5565b29c140e)
![3 12 30 00 PM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/b25639bb-cc2b-4141-8495-9f78e67a99dd)
![4 12 30 00 PM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/3785a0aa-404b-4a02-bb63-64087e38ee0a)
![5 12 30 00 PM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/22f1503d-f737-41dc-b301-7c7ec61432a9)
![6 12 30 00 PM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/61d96586-de75-404a-83b5-723847518355)
![7 12 29 56 PM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/cbba6ca5-afa2-41b4-9620-180312749934)
![8 12 30 02 PM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/4cf2f9ea-2928-4d1a-bc5b-549902875ed5)
![9 12 30 02 PM](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/a6adbc47-29eb-4385-9622-145be591c04f)
![10](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/2eabe8e2-04da-40d2-9774-3d2c5cb2893d)
![11](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/adce5e5c-2906-4545-be31-dfcb08f6cd55)
![12](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/e7e4d4ae-25f1-4729-b04b-07301c0976da)
![13](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8e679968-3290-483f-9c02-40d60141dbc6)
![14](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/0d50d8c7-906e-4077-bfdc-b8a65f12229b)
![15](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/f0f4743b-dcdb-4c7a-bff4-4d666460b84b)
![16](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/3700557d-12c5-4194-9180-604453871124)
![17](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/c4cb83ba-d5ea-4fba-be2b-451679322283)
![18](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/7a6edbbe-e950-42ec-8835-6bf8b961ddf5)
![19](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/293c7c5e-e765-4a38-b679-035672f8d97e)
![20](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/cc333d1f-7050-42b3-acd0-74f66888e26f)
![21](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/5c235e78-04f5-45ea-bbb6-ac4d43f1d3d5)
![22](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8db74fe6-41f4-46c1-87dc-c35091421ab3)
![23](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/e5d31e71-d384-43d2-9917-cfabe07d14b3)
![24](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/d6bae0c3-a256-498b-9be8-e0f3824e1fbc)
![25](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/6e71a37c-144f-4c6f-9d3e-9ffbf7f6c859)
![26](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/922b9950-d116-44e9-8778-9d75515bcadb)
![27](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/276f9686-6dbc-4fa9-91f0-b2743abec8c3)
![28](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/7056f671-11c5-4be4-98a0-b2db5bdb3748)
![29](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/03109fdd-d147-4a96-a3d4-b3d2fab278bb)
![30](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/51eda2a1-0d48-4a53-bca3-70da913e4fbf)
![31](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/000508ed-6ebb-4b2d-9d04-d73df0563163)
![32](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/bb145d02-eef2-4c0e-8009-9210dce216d6)
![33](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/7c24c183-8d34-4669-9921-005869b92a92)
![34](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8ebdf2ac-18c0-4eaa-8d78-64d6db4b8848)


## Findings 

## Conclusion
In a nutshell, the Chicago White Sox team is recommended to use the best lineup in the coming season in 2023. Based on the findings of our analysis, using the best lineup can lead to a higher average run scored compared to the actual 2022 season. 

Higher expected runs scored are generally associated with higher variability (standard deviation) in the lineup’s performance. For this reason, the team should be mindful of the potential risks and uncertainties associated with pursuing higher runs scored and take those changes into account when making strategic decisions.

Relying solely on the most expensive players within a lineup to achieve the highest runs is not a prudent strategy for the Chicago White Sox team. Although high-priced players are often considered to be better, the team's success is not solely determined by individual talent or payroll. Instead, other factors such as team synergy, coordination, and collective effectiveness can also influence the team's ability to score runs and win games. Therefore, the team should focus on building a cohesive and effective team that can perform well together, rather than relying solely on spending more money on players.

## Takeaways
* Lineups with high win rate are typically found in the middle class of payroll.
* Higher payrolls are not generally associated with higher win rate.
* When pursuing higher run scored, the team should carefully consider how changes in standard deviation can affect their results.

## Discussions
Hirotsu, N. (2011) indicated that when changing batting order with the same players, an increase in runs scored led to an increase in standard deviation. Our own simulation corroborated this finding, as we observed substituting players also resulted in an increase in standard deviation when there is an increase in runs scored. However, our simulation was conducted using a modified batting order strategy. Therefore, to gain a more comprehensive understanding of the impact of changing the batting order on standard deviation, further investigations can be conducted using different batting orders. By using this model, the Chicago White Sox team can determine whether substituting players or changing the batting order has a greater impact on standard deviation when aiming for higher runs scored.  This would provide valuable insights for the team to make informed decisions regarding their batter substitution strategy and optimize their performance on the field.

## Reference
* Ursin, D. (2014). A MARKOV MODEL FOR BASEBALL WITH APPLICATIONS.
* Hirotsu, N. (2011). Reconsideration of the best batting order in baseball: Is the order to maximize the expected number of runs really the best? Journal of Quantitative Analysis in Sports, 7(2). doi:10.2202/1559-0410.1332
* 2023 Chicago White Sox White Sox Roster & Staff. (n.d.). Retrieved May 6, 2023, from https://www.mlb.com/whitesox/roster

## Project Team
* Jhe Yu (Lawrence) Lin
* Lok I (Minnie) Lou 
* HOI KEI (Joanne) TANG
