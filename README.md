# Scheme Eligibility Prediction for NSAP Using Machine Learning

## Overview
This project automates the classification of National Social Assistance Programme (NSAP) schemes using **Machine Learning** deployed on **IBM Cloud**. It helps government agencies quickly and accurately determine the most suitable scheme for applicants based on their demographic and socio-economic data, replacing manual classification processes that are time-consuming and error-prone.

## Problem Statement
The National Social Assistance Program (NSAP) is a flagship social security and welfare program by the Government of India. It aims to provide financial assistance to the elderly, widows, and persons with disabilities belonging to below-poverty-line (BPL) households. The program consists of several sub-schemes, each with specific eligibility criteria. Manually verifying applications and assigning the correct scheme is often time-consuming and error-prone, delaying financial aid for deserving individuals.  
This project focuses on designing and evaluating a multi-class classification model that accurately predicts the most appropriate NSAP scheme for an applicant based on their demographic and socio-economic data.

## Proposed Solution
The solution was implemented using **IBM Watsonx.ai Studio AutoAI** on IBM Cloud to:
- Import and preprocess NSAP dataset  
- Automatically generate ML pipelines and select the best-performing algorithm  
- Deploy the model as a REST API for real-time predictions  

## System Approach
- **System Requirements**  
  - IBM Cloud account with Watsonx.ai Studio Lite  
  - AutoAI for automated pipeline generation and evaluation  
  - Cloud Object Storage for dataset hosting  
  - Deployment space for model deployment and testing  

- **Libraries & Tools Used**  
  - IBM Watsonx.ai AutoAI (Random Forest, Decision Tree)  
  - Python for data visualization and API testing  
  - REST API for real-time predictions  

## Algorithm & Deployment

### Algorithm Selection
**Snap Random Forest Classifier** was chosen as the best-performing algorithm.  
Random Forest is an ensemble learning method that builds multiple decision trees and combines their outputs to improve prediction accuracy and reduce overfitting. It is highly effective for multi-class classification problems.

### Data Input
The model used demographic and socio-economic attributes of applicants such as statename, districtname etc.

### Training Process
The dataset was split into training and test sets using AutoAI. Multiple pipelines were generated and hyperparameter tuning was applied automatically to select the optimal pipeline.

### Prediction Process
The final trained model predicts the correct NSAP scheme for each applicant. The model was deployed as a REST API on IBM Cloud, enabling real-time predictions from external systems.

## Results
The deployed model achieved high classification accuracy with reliable performance across multiple metrics. Below are screenshots of the steps and results:

1. **Dataset Upload**  
   ![Dataset Upload](https://res.cloudinary.com/dya8ig3jg/image/upload/v1754314003/db-upload_us2eb7.png)

2. **AutoAI Pipeline Generation**  
   ![AutoAI Pipeline](https://res.cloudinary.com/dya8ig3jg/image/upload/v1754314004/autoai-pipeline_ctylbj.png)

3. **Model Evaluation Metrics**  
   ![Model Evaluation](https://res.cloudinary.com/dya8ig3jg/image/upload/v1754314003/model-evaluation_lrus02.png)

4. **Confusion Matrix**  
   ![Confusion Matrix](https://res.cloudinary.com/dya8ig3jg/image/upload/v1754314054/confusion-matrix_mtwjk2.png)

5. **Testing Prediction**  
   ![API Test Screenshot](https://res.cloudinary.com/dya8ig3jg/image/upload/v1754314184/test-prediction_fjxfuw.png)

6. **Final Output**  
   ![Output Interface](https://res.cloudinary.com/dya8ig3jg/image/upload/v1754314183/final-output_ftj4y5.png)

## Conclusion
This project demonstrates the potential of cloud-based machine learning to automate scheme eligibility classification, improving the speed and accuracy of social welfare service delivery. By leveraging IBM Cloud and Watson Studio AutoAI, the solution is scalable, easy to deploy, and integrates seamlessly with existing government systems.

## Future Scope
- Integrate additional socio-economic datasets for enhanced prediction accuracy  
- Explore advanced deep learning models for more complex eligibility criteria  
- Scale deployment to cover multiple states and nationwide integration  
- Use edge computing for faster on-site predictions and low-latency processing  

## References
1. [AI Kosh NSAP Dataset](https://aikosh.indiaai.gov.in/web/datasets/details/district_wise_pension_data_under_the_national_social_assistance_programme_nsap_1.html)
2. [IBM Cloud Watson Studio](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/welcome-main.html?context=wx&audience=wdp)
3. Breiman, L. (2001). Random Forests. Machine Learning, 45(1), 5–32.
4. [NSAP Official Website](https://nsap.nic.in)