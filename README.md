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
  - [Live demo](#live-demo)
- [About this template](#about-this-template)
  - [Contributing](#contributing)
  - [Versioning](#versioning)
  - [Authors](#authors)
  - [License](#license)
  - [Acknowledgments](#acknowledgments)

_INSTRUCTIONS: Complete all required deliverable sections below._

## Project summary

### The issue we are hoping to solve

Water contamination is becoming major issue due to :
a) Sewage lines getting mixed with the potable residential water lines  
b) Hazardous/Industrial sewage getting disposed either in open places or in water bodies 
Our solution would check the contamination of water by measuring water quality at sampling points

### How our technology solution can help

Our solution would display the water potability result based on the sampling data fed to the solution

### Our idea

Water quality assessment is the process of evaluating the physical, chemical, and biological characteristics of water to determine its suitability for a specific purpose. This can include drinking water, irrigation, recreation, and industrial use. Water quality assessment is important for protecting human health and the environment.
Water quality assessment is important for identifying and managing water pollution risks. It can also be used to track changes in water quality over time and to evaluate the effectiveness of water treatment and management programs.
How is water quality assessed?
Water quality assessment typically involves collecting water samples from different locations and testing them for a variety of parameters. These parameters may include physical parameters such as pH value, Hardness, Solids, Chloramines, Sulfates, Conductivity, Organic Carbon, Trihalomethanes, Turbidity.
The results of the water quality tests are compared to established standards to determine whether the water is suitable for its intended use. For example, drinking water must meet certain standards for microbiological, chemical, and physical quality.
Solution proposed by team:
Dataset: Gather water quality data from various sources, including sensors, government databases, or field measurements. Ensure the data includes parameters like pH value, Hardness, Solids, Chloramines, Sulfates, Conductivity, Organic Carbon, Trihalomethanes, Turbidity. But these parameters have been already monitored and gathered in the form of datasets which are available online. One such dataset was used for training the model. Link: Water Quality (kaggle.com)
Platform: IBM Cloud provides a range of cloud services and solutions that cater to businesses and developers looking to build, deploy, and manage applications and services in the cloud. It offers a suite of AI and machine learning services, including IBM Watson, to help businesses build and deploy AI-powered applications. A project named “Water Quality Assessment” was created along with Machine Leaning resource and was integrated with project. Further, dataset was added to the project for processing. 
Model Processing and Training: IBM WatsonX has been one of the leading AI and data platform. It provides one stop complete solution for AI model processing. One of the service is AutoML. It is tool that streamlines the process of developing machine learning models. AutoML was used as the primary resource integrated with Machine Learning Instance. The dataset was fed to AutoML and the training was started. It automatically trains over numerous algorithms and lists the best accuracy model.
Deployment: The model after training was tested with manual inputs. For deployment, we have created a Deployment Space and in the deployment space the model was deployed. WatsonX provides autogenerated code in different languages to ease the process of integration. This deployed model can be access to endpoints.
User Interface: We have used ReactJS for front-end and python Flask for back-end. The front-end runs on port 3000 and provides a form where the user can provide inputs for different parameters used of water quality assessments. These inputs are provided to the model deployed on cloud by the back-end built using Flask server. The flask server runs on port 2000 which redirects all the inputs to model. After the user fills all the details and clicks submit button, the model receives the inputs and predicts whether the water is potable or not. The result is displayed after the processing is done.

More detail is available in our [description document](./docs/DESCRIPTION.md).

## Technology implementation

### IBM AI service(s) used

_INSTRUCTIONS: Included here is a list of commonly used IBM AI services. Remove any services you did not use, or add others from the linked catalog not already listed here. Leave only those included in your solution code. Provide details on where and how you used each IBM AI service to help judges review your implementation. Remove these instructions._

- [IBM Natural Language Understanding](https://cloud.ibm.com/catalog/services/natural-language-understanding) - WHERE AND HOW THIS IS USED IN OUR SOLUTION
- [Watson Assistant](https://cloud.ibm.com/catalog/services/watson-assistant) - WHERE AND HOW THIS IS USED IN OUR SOLUTION
- [Watson Discovery](https://cloud.ibm.com/catalog/services/watson-discovery) - WHERE AND HOW THIS IS USED IN OUR SOLUTION
- [Watson Speech to Text](https://cloud.ibm.com/catalog/services/speech-to-text) - WHERE AND HOW THIS IS USED IN OUR SOLUTION
- [Watson Text to Speech](https://cloud.ibm.com/catalog/services/text-to-speech) - WHERE AND HOW THIS IS USED IN OUR SOLUTION
- List any additional [IBM AI services](https://cloud.ibm.com/catalog?category=ai#services) used or remove this line

### Other IBM technology used

INSTRUCTIONS: List any other IBM technology used in your solution and describe how each component was used. If you can provide links to/details on exactly where these were used in your code, that would help the judges review your submission.

### Solution architecture

Diagram and step-by-step description of the flow of our solution:

![Video transcription/translaftion app](https://developer.ibm.com/developer/tutorials/cfc-starter-kit-speech-to-text-app-example/images/cfc-covid19-remote-education-diagram-2.png)

1. The user navigates to the site and uploads a video file.
2. Watson Speech to Text processes the audio and extracts the text.
3. Watson Translation (optionally) can translate the text to the desired language.
4. The app stores the translated text as a document within Object Storage.

## Presentation materials

_INSTRUCTIONS: The following deliverables should be officially posted to your My Team > Submissions section of the [Call for Code Global Challenge resources site](https://cfc-prod.skillsnetwork.site/), but you can also include them here for completeness. Replace the examples seen here with your own deliverable links._

### Solution demo video

[![Watch the video](https://raw.githubusercontent.com/Liquid-Prep/Liquid-Prep/main/images/readme/IBM-interview-video-image.png)](https://youtu.be/vOgCOoy_Bx0)

### Project development roadmap

The project currently does the following things.

- Feature 1
- Feature 2
- Feature 3

In the future we plan to...

See below for our proposed schedule on next steps after Call for Code 2023 submission.

![Roadmap](./images/roadmap.jpg)

## Additional details

_INSTRUCTIONS: The following deliverables are suggested, but **optional**. Additional details like this can help the judges better review your solution. Remove any sections you are not using._

### How to run the project

INSTRUCTIONS: In this section you add the instructions to run your project on your local machine for development and testing purposes. You can also add instructions on how to deploy the project in production.

### Live demo

You can find a running system to test at...

See our [description document](./docs/DESCRIPTION.md) for log in credentials.

---

_INSTRUCTIONS: You can remove the below section from your specific project README._

## About this template

### Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

### Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

### Authors

<a href="https://github.com/Call-for-Code/Project-Sample/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=Call-for-Code/Project-Sample" />
</a>

- **Billie Thompson** - _Initial work_ - [PurpleBooth](https://github.com/PurpleBooth)

### License

This project is licensed under the Apache 2 License - see the [LICENSE](LICENSE) file for details.

### Acknowledgments

- Based on [Billie Thompson's README template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2).
