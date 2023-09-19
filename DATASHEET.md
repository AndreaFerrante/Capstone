# **Datasheet for the Credit Card Default Clients**

   - **Title**: Default of Credit Card Clients Dataset
   - **Version**: 1.0 (assuming no updates have been made to the dataset since its initial release)
   - **Dataset URL**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients)
   - **Permanent Identifier**: Not available
   - **Creators**: I-Cheng Yeh and Che-hui Lien
   - **Funders**: Not specified
   - **Date of Creation**: 2005
   - **Update Frequency**: Not applicable (single release)
   - **Dataset License**: Not specified, but it is publicly available on the UCI repository which generally hosts datasets that are freely available for research purposes.
   
## **Motivation**

   - **Purpose**: The dataset was created to facilitate research in credit default prediction, a critical area in financial risk management.
   - **Creators and Funders**: The dataset was created by I-Cheng Yeh with the collaboration of Che-hui Lien. The exact entity funding the creation is not specified.

## **Composition**

   - **Instances Represent**: Each instance represents a credit card client with various attributes related to their credit history, demographic information, and whether they defaulted in the next month.
   - **Number of Instances**: There are 30,000 instances in the dataset.
   - **Missing Data**: There is no indication of missing data in the dataset description.
   - **Confidential Data**: The dataset does not contain personally identifiable information, but it does contain sensitive financial data, which is presumably anonymized.

## **Collection Process**

   - **Data Acquisition**: The data was acquired from credit card clients in Taiwan from April 2005 to September 2005. The exact method of data collection is not specified.
   - **Sampling Strategy**: The dataset appears to be a sample of a larger subset, but the exact sampling strategy is not detailed in the dataset description.
   - **Time Frame**: The data spans from April 2005 to September 2005.

## **Preprocessing/Cleaning/Labeling**

   - **Preprocessing**: The dataset description does not provide detailed information on preprocessing, cleaning, or labeling processes undertaken before the dataset was compiled. However, it is structured and categorized with labeled attributes, indicating some level of preprocessing.
   - **Raw Data**: It is not clear if the raw data is saved in addition to the preprocessed data.

## **Uses**

   - **Other Tasks**: Apart from credit default prediction, the dataset can potentially be used for demographic analysis, financial behavior analysis, and to develop credit scoring algorithms.
   - **Impact on Future Uses**: The dataset contains sensitive financial data, and while it is anonymized, it should be used responsibly to avoid potential risks such as unfair stereotyping or discrimination. Users should be cautious about how the results derived from this dataset are applied, especially in real-world applications that could affect individuals' financial standings.
   - **Tasks for Which the Dataset Should Not Be Used**: The dataset should not be used for any task that could potentially lead to the identification of individuals or for tasks that could facilitate discriminatory practices.

## Detailed Data Dictionary

- **Instances**: 30,000
- **Attributes**: 24
- **Attribute Information**:
  - **ID**: ID of each client
  - **LIMIT_BAL**: Amount of given credit in NT dollars (includes individual and family/supplementary credit)
  - **SEX**: Gender (1 = male; 2 = female)
  - **EDUCATION**: Education (1 = graduate school; 2 = university; 3 = high school; 4 = others)
  - **MARRIAGE**: Marital status (1 = married; 2 = single; 3 = others)
  - **AGE**: Age in years
  - **PAY_0** to **PAY_6**: History of past payment. We tracked the past monthly payment records (from April to September, 2005) as follows: PAY_0 = the repayment status in September, 2005; PAY_1 = the repayment status in August, 2005; ...;PAY_6 = the repayment status in April, 2005. The measurement scale for the repayment status is: -1 = pay duly; 1 = payment delay for one month; 2 = payment delay for two months; ...; 8 = payment delay for eight months; 9 = payment delay for nine months and above.
  - **BILL_AMT1** to **BILL_AMT6**: Amount of bill statement (BILL_AMT1 = amount of bill statement in September, 2005; BILL_AMT2 = amount of bill statement in August, 2005; ...; BILL_AMT6 = amount of bill statement in April, 2005).
  - **PAY_AMT1** to **PAY_AMT6**: Amount of previous payment (PAY_AMT1 = amount paid in September, 2005; PAY_AMT2 = amount paid in August, 2005; ...; PAY_AMT6 = amount paid in April, 2005).
  - **default.payment.next.month**: Default payment (1 = yes, 0 = no)

## **Distribution**

   - **Distribution**: The dataset has been distributed through the UCI Machine Learning Repository, a popular platform for sharing datasets for research and educational purposes.
   - **Copyright/IP/ToU**: The exact terms of use or copyright details are not specified on the dataset page. It is generally assumed that datasets on the UCI repository are available for research and educational uses, but it would be prudent to verify any specific restrictions before using the dataset for commercial purposes.
