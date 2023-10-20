[![License](https://img.shields.io/badge/License-Apache2-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0) [![Community](https://img.shields.io/badge/Join-Community-blue)](https://developer.ibm.com/callforcode/solutions/projects/get-started/)

_INSTRUCTIONS: This GitHub repository serves as a template you can use to create a new project for the [2023 Call for Code Global Challenge](https://developer.ibm.com/callforcode/global-challenge/). Use the **Use this template** button to create a new version of this repository and start entering content for your own Call for Code submission project. Make sure you have [registered for the 2023 Call for Code Global Challenge](https://developer.ibm.com/callforcode/global-challenge/register/) to access resources and full project submission instructions. Remove any "INSTRUCTIONS" sections when you are ready to submit your project._

_New to Git and GitHub? This free online course will get you up to speed quickly: [Getting Started with Git and GitHub](https://www.coursera.org/learn/getting-started-with-git-and-github)_.

# Potable Water Sustainability


- [Project summary](#project-summary)
  - [The issue we are hoping to solve](#the-issue-we-are-hoping-to-solve)
  - [How our technology solution can help](#how-our-technology-solution-can-help)
  - [Our idea](#our-idea)
- [Technology implementation](#technology-implementation)
  - [IBM AI service(s) used](#ibm-ai-services-used)
  - [Other IBM technology used](#other-ibm-technology-used)
  - [Solution architecture](#solution-architecture)
- [Presentation materials](#presentation-materials)
  - [Solution demo video](#solution-demo-video)
  - [Project development roadmap](#project-development-roadmap)
- [Additional details](#additional-details)
  - [How to run the project](#how-to-run-the-project)

## Project summary

### The issue we are hoping to solve

Water contamination is becoming major issue due to :
a) Sewage lines getting mixed with the potable residential water lines  
b) Hazardous/Industrial sewage getting disposed either in open places or in water bodies <br>
Our solution would check the contamination of water by measuring water quality at sampling points.

### How our technology solution can help

Our solution would display the water potability result based on the sampling data fed to the solution.

### Our idea

Water quality assessment is the process of evaluating the physical, chemical, and biological characteristics of water to determine its suitability for a specific purpose. This can include drinking water, irrigation, recreation, and industrial use. Water quality assessment is important for protecting human health and the environment.
Water quality assessment is important for identifying and managing water pollution risks. It can also be used to track changes in water quality over time and to evaluate the effectiveness of water treatment and management programs.<br>
**How is water quality assessed**?<br>
Water quality assessment typically involves collecting water samples from different locations and testing them for a variety of parameters. These parameters may include physical parameters such as pH value, Hardness, Solids, Chloramines, Sulfates, Conductivity, Organic Carbon, Trihalomethanes, Turbidity.
The results of the water quality tests are compared to established standards to determine whether the water is suitable for its intended use. For example, drinking water must meet certain standards for microbiological, chemical, and physical quality.<br>
**Solution proposed by team**:<br>
**Dataset**: Gather water quality data from various sources, including sensors, government databases, or field measurements. Ensure the data includes parameters like pH value, Hardness, Solids, Chloramines, Sulfates, Conductivity, Organic Carbon, Trihalomethanes, Turbidity. But these parameters have been already monitored and gathered in the form of datasets which are available online. One such dataset was used for training the model. Link: Water Quality (kaggle.com)<br>
**Platform**: IBM Cloud provides a range of cloud services and solutions that cater to businesses and developers looking to build, deploy, and manage applications and services in the cloud. It offers a suite of AI and machine learning services, including IBM Watson, to help businesses build and deploy AI-powered applications. A project named “Water Quality Assessment” was created along with Machine Leaning resource and was integrated with project. Further, dataset was added to the project for processing. <br>
**Model Processing and Training**: IBM WatsonX has been one of the leading AI and data platform. It provides one stop complete solution for AI model processing. One of the service is AutoML. It is tool that streamlines the process of developing machine learning models. AutoML was used as the primary resource integrated with Machine Learning Instance. The dataset was fed to AutoML and the training was started. It automatically trains over numerous algorithms and lists the best accuracy model.<br>
**Deployment**: The model after training was tested with manual inputs. For deployment, we have created a Deployment Space and in the deployment space the model was deployed. WatsonX provides autogenerated code in different languages to ease the process of integration. This deployed model can be access to endpoints.<br>
**User Interface**: We have used ReactJS for front-end and python Flask for back-end. The front-end runs on port 3000 and provides a form where the user can provide inputs for different parameters used of water quality assessments. These inputs are provided to the model deployed on cloud by the back-end built using Flask server. The flask server runs on port 2000 which redirects all the inputs to model. After the user fills all the details and clicks submit button, the model receives the inputs and predicts whether the water is potable or not. The result is displayed after the processing is done.<br>

## Technology implementation

### IBM AI service(s) used

**Watsonx** :-
Watsonx was used in our solution as it acts like a platform where we can train and deploy machine learning model. Under watsonx we created a project for testing water potability. Watsonx instance was linked with a cloud storage object  and it provided use storage to upload and save datasets. Watsonx provided us the capability to properly visualise the dataset using tools like historgram, line graph, scatterplots etc. It also provided us with assets like auto ai experiment to train our models. Finally watsonx also provided us the capability to store the trained model and deploy it.<br>
Under watsonx we used the following services<br>
1. **Auto Ai experiment**:- Auto AI experiment provides a platform to train and build models. We used a foundation binary classifier model. The binary classifier   model was trained in 9 pipelines and hence its generated 9 different models. We used the model with the highest accuracy of around 66%. The model was of type P4-XGB classifier model.<br>
2. **Watsonx deployments**:- The model was deployed using deployment facility provided by IBM watsonx. Once the model was deployed , we could access it making use of API keys and access tokens.

### Other IBM technology used

- **Cloud Storage Object**:- IBM cloud storage object was created and linked to watsonx. Cloud storage object was used to store the training datasets ie the CSV files. The model trained by the auto ai experiment was also stored in the cloud storage object.

### Solution architecture

Diagram and step-by-step description of the flow of our solution:

![Water Quality (2)](https://github.com/Aman-Surkar/Potable-Water-Sustainability/assets/99606590/8f12fa75-f27b-4bee-97e1-07c1334cb522)

1. Upload Dataset.
2. WatsonX's sub-service Auto Ai trains the dataset and creates a model.
3. Trained model is deployed in Deployment Space. This deployment is accessible using endpoints.
4. The UI-Frontend gets input from user and sends them to backend flask server.
5. The Flask server redirects the inputs to model, the model predicts the outcome on the basis of the inputs.
6. The user gets the result displayed over the frontend.

## Presentation materials

### Solution demo video

https://youtu.be/a8_oS8rFrSc?si=GqtF_KQo3QYfI9g2

### Project development roadmap

The project currently does the following things.

- Generates predictive model
- Gets inputs from user
- Predicts outcome using the inputs

![Project devlopment roadmap_page-0001](https://github.com/Aman-Surkar/Potable-Water-Sustainability/assets/99606590/a2f73ad0-02ef-4445-988b-d97b6c90293a)

![Project devlopment roadmap_page-0002](https://github.com/Aman-Surkar/Potable-Water-Sustainability/assets/99606590/5f88fd55-cae2-483e-8270-eaed831110e5)

### How to run the project

- Clone the repo git clone https://github.com/smartvibs8876/WaterPotabilityBackEndFlask.git
- Navigate to the project cd WaterPotabilityBackEndFlask
- Install dependencies pip install -r requirements.txt
- Run the script python script.py
- App will run on localhost port 2000. So hit localhost:2000 in browser

---


