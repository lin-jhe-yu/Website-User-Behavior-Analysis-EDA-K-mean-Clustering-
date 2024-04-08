<img width="1501" alt="Screen Shot 2024-04-02 at 3 22 32 PM" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/108fb197-e8eb-4339-b2c8-3d841ba0f807">

# Website User Behavior Analysis
Taiwan ICDF Bamboo Industrialization Project in Guatemala is dedicated to fostering sustainable bamboo industries throughout Guatemala. Our mission involves offering comprehensive technical assistance to industry participants, empowering them with the knowledge and skills needed to thrive in this sector.

To achieve our goals, we use the Bamboo Industrialization Project website as a platform for introducing and promoting our projects. Through this online platform, we aim to raise awareness about the project, its objectives, and the opportunities it presents for individuals and communities. Moreover, we seek to encourage greater participation in the bamboo industry by extending invitations to interested stakeholders to join our cause and contribute to its success.

## Problem Description
We are facing many challenges in terms of brand awareness and increasing the number of participants from the existing bamboo industry. By analyzing website user behavior, we aim to gain insights into our website visitors and their interactions with our platform. With this understanding, we can offer tailored suggestions to enhance our website content and improve user experience.

## Exploratory Data Analysis
The dataset covers January 15th, 2024 to March 15th, 2024, totaling 8743 activity records. After thorough organization and sorting, we've condensed this information into 804 user data (see Table 1). 

On average, people spend about 76 seconds engaging with content, with the midpoint at around 29 seconds. When it comes to website interactions, website users typically perform around 11 actions (including page loads, link clicks, etc), and the median is closer to 7 (see Table 2). There are quite a few users who show significantly higher engagement levels (time and events) compared to the average (see Figures 1 and 2).

Approximately 68 percent of users are from Guatemala, with the USA following behind at 14 percent (see Figure 3). Visitors with longer user engagement tend to have more events and engage more on page {Construcción con Bambú} and page {Proyecto de Industrialización del Bambú en Guatemala}. In addition, visitors with more event count tend to engage more on page {Introducción al plan de bambú} and {Plan de bambú} (see Figure 4).

#### Table 1: User data
![user data dataframe](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/2f27c56d-0a97-4d83-bad4-812e3b7a56e0)

#### Table 2: User data summary
![user data summary](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/55a4854b-81fc-44b4-a193-f5c7f8a8fd89)

#### Figure 1: User engagement distribution
<img width="800" alt="30" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/d6886ab0-8d3e-4083-a091-f385a3f2d94c">

#### Figure 2: Event count distribution
<img width="800" alt="30" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/60bfd2fb-2058-497f-9629-1327346ea23c">

#### Figure 3: Geographical information pie chart
<img width="500" alt="30" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/33913a9b-e4df-4cbe-bef8-f2c4678c7470">
<img width="230" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8aee6717-0a5e-416f-a1bd-b438cbb165e9">

#### Figure 4: Correlation Matrix
<img width="800" alt="50" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/71435e82-ee69-4962-a084-3e6824d0b130">

## Feature Engineering
Principal component analysis (PCA) is a commonly used dimension reduction technique in data engineering. It can save computation time and reduce model complexity and noise. Therefore, we chose to employ PCA on our data. We proceeded with the following steps: data standardization (see Table 3), principal component selection (see Figures 5 and 6), and data transformation (see Table 4). After standardizing data, we selected 17 principal components, which explain around 70 percent of the total variance in the original data. Subsequently, data were transformed with principal components.

#### Table 3: Standardizing data
![standardized user data](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/26ff864f-2d60-4622-b874-a7b4f3477905)

#### Figure 5: Principal components composition
<img width="500" alt="30" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/f2d1ce05-3667-4e2e-b5a1-297e3200ddbb">

#### Figure 6: Selecting the number of principal components
<img width="500" alt="30" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/45ce3a76-f69e-4ede-b7d4-c80ca0641e5a">
<img width="350" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/378b1a56-da9c-4d9b-8e9f-73ecd02e3a94">

#### Table 4: Transforming data
<img width="900" alt="pca" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8029e0a5-08c4-48a3-9e91-42d566c46981">

## Model Building and Evaluation
We tried out K-means clustering models with cluster parameters from 1 to 20 and calculated their within-cluster-sum-of-square (WCSS) values. However, there was no clear elbow point.  Therefore, we subsequently employed the silhouette method. The highest silhouette score was achieved with 2 clusters. We then consider tuning the number of clusters to 2 might produce optimal clustering for our analysis. 

#### Figure 7: The elbow method
![elbow method](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/cee0f6f1-300a-4370-bea5-02e751ade0f2)

#### Figure 8: The silhouette method
![silhouette method](https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/b77695f7-c497-42df-a464-0445bb1f2cae)

## Results and cluster exploration
After applying K-means clustering with 2 clusters, 764 users were classified as cluster 0 and 40 users as cluster 1 (see Figure 9). Cluster 0 constitutes 95% of the user group, while cluster 0 only accounts for nearly 5%. PCA is the most powerful component to distinguish the cluster (see Figure 10). Users from both cluster 0 and cluster 1 spend more than half of their time on our website browsing the first page, on average. 

For Cluster 0, the top 5 topics are: [Proyecto de Industrialización del Bambú en Guatemala], [Construcción con Bambú], [Bambú en la Moda], [Invernadero construido a base de bambú industrializado] and [Construcción]. Cluster 1 shares the same top 3 topics, followed by [Guatemala lidera industrialización y aprovechamiento del Bambú en Centro América], [Artesanas y panaderas, mujeres de Chiquimula buscan alternativas económicas] (see Table 5). The users from cluster 1 spend significant longer time on each topic except [Savenhouse built from industrialized bamboo], [Bamboo in Fashion], [Fertilización de plantación en finca Sabana Grande FAUSAC Escuintla], and [Noticias y Eventos| Proyecto de Industrialización del Bambú en Guatemala] (see Table 6 and Figures 11 to 44). 

#### Cluster characteristics:
Cluster 0
* represents 95% of the customer base.
* interested in the application of bamboo.
* interested in homepage of construction with bamboo, Bambú en la Moda.

Cluster 1
* represents 5% of the customer base.
* interested in the project itself.
* spends significant longer time on our webiste.
* interested in homepage of construction with bamboo, Bambú en la Moda.

#### Figure 9: User cluster pie chart
<img width="413" alt="Screen Shot 2024-04-03 at 11 14 09 AM" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/d8108b8f-eab3-46cf-baf3-77dc122190ac">

#### Figure 10: Cluster scatter plot
<img width="300" alt="cluster scatter plot" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/873aa75a-023b-4a65-9c90-e9ed2d7def86">
<img width="300" alt="cluster scatter plot" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/f79771f1-6d3c-4d6b-85cb-744d04a9a8a0">
<img width="300" alt="cluster scatter plot" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8fa51316-ad54-41ef-a800-0d7261fb61b9">
<img width="300" alt="cluster scatter plot" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/0935f478-7555-46f8-95f1-4aa0c8ff2c86">
<img width="300" alt="cluster scatter plot" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/eca21c41-c959-424b-9e31-4c6d4c37e806">
<img width="300" alt="cluster scatter plot" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/3672127f-4b2c-40de-9521-31acf19a9976">
<img width="300" alt="cluster scatter plot" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/a981793c-8af0-401a-bcaa-23b2ffaa51e7">
<img width="300" alt="cluster scatter plot" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/389ccfc5-19a6-4370-b360-20fc5d6cfa1f">

#### Table 5: Topic ranking 
<img width="800" alt="Screen Shot 2024-04-05 at 3 24 38 PM" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/c983ff75-85b8-415a-acca-a45edb839795">

#### Table 6: Cluster summary
<img width="600" alt="pca" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/d19595d9-ba23-4fda-b6e8-9bb9e8ddb227">

#### Figure 11 to Figure 44: Cluster data histogram
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/78fa7ca9-ff6f-4727-8ebb-198752c629d0">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/de2291bc-89ee-4151-998b-5565b29c140e">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/b25639bb-cc2b-4141-8495-9f78e67a99dd">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/3785a0aa-404b-4a02-bb63-64087e38ee0a">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/22f1503d-f737-41dc-b301-7c7ec61432a9">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/61d96586-de75-404a-83b5-723847518355">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/cbba6ca5-afa2-41b4-9620-180312749934">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/4cf2f9ea-2928-4d1a-bc5b-549902875ed5">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/a6adbc47-29eb-4385-9622-145be591c04f">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/2eabe8e2-04da-40d2-9774-3d2c5cb2893d">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/adce5e5c-2906-4545-be31-dfcb08f6cd55">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/e7e4d4ae-25f1-4729-b04b-07301c0976da">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8e679968-3290-483f-9c02-40d60141dbc6">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/0d50d8c7-906e-4077-bfdc-b8a65f12229b">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/f0f4743b-dcdb-4c7a-bff4-4d666460b84b">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/3700557d-12c5-4194-9180-604453871124">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/c4cb83ba-d5ea-4fba-be2b-451679322283">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/7a6edbbe-e950-42ec-8835-6bf8b961ddf5">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/293c7c5e-e765-4a38-b679-035672f8d97e">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/cc333d1f-7050-42b3-acd0-74f66888e26f">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/5c235e78-04f5-45ea-bbb6-ac4d43f1d3d5">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8db74fe6-41f4-46c1-87dc-c35091421ab3">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/e5d31e71-d384-43d2-9917-cfabe07d14b3">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/d6bae0c3-a256-498b-9be8-e0f3824e1fbc">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/6e71a37c-144f-4c6f-9d3e-9ffbf7f6c859">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/922b9950-d116-44e9-8778-9d75515bcadb">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/276f9686-6dbc-4fa9-91f0-b2743abec8c3">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/7056f671-11c5-4be4-98a0-b2db5bdb3748">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/03109fdd-d147-4a96-a3d4-b3d2fab278bb">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/51eda2a1-0d48-4a53-bca3-70da913e4fbf">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/000508ed-6ebb-4b2d-9d04-d73df0563163">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/bb145d02-eef2-4c0e-8009-9210dce216d6">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/7c24c183-8d34-4669-9921-005869b92a92">
<img width="300" alt="20" src="https://github.com/lin-jhe-yu/Website-User-Behavior-Analysis-EDA-K-mean-Clustering-/assets/121969452/8ebdf2ac-18c0-4eaa-8d78-64d6db4b8848">

## Findings 
* There are two website user groups. Cluster 0 makes up the majority (95%), while Cluster 1 spends significantly more time on the website.
* Both clusters share a mutual interest in the homepage of construction with bamboo, Bambú en la Moda.
* The two clusters have a slightly different focus. Cluster 0 mainly browses pages related to bamboo applications at all areas. Cluster 1 is more interested in the project itself, such as services we offer and events we host.
* The homepage is crucial for sharing information effectively. Both clusters allocate a significant portion of their browsing time to the homepage (Cluster 0 spending 45.88% and Cluster 1 devoting 57.84%).


## Suggestion
1. Focus on updating the information regarding bamboo construction and fashion.
2. To seek for potenial particpant, we can target cluster 1. Enhance the service we provide regarding construction to target cluster 1 to cooperate with our project, enhancing make it more informative.
3. 
Cluster 0:
* 
*
*
Cluster 1: 
* 
* 

## Project Team
* Jhe Yu (Lawrence) Lin
