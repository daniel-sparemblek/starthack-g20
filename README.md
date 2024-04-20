
## Project Forestify: Revolutionizing Wildfire Management in Brazil (Case from START Hack 2024)

### 1. Introduction

#### What is START Hack?
[START Hack](https://www.startglobal.org/start-hack/home) is a Europe's most entrepreneurial hackathon, bringing in 600+ hackers from top European universities. Hackers have 3 hours to develop solutions to problems provided by case partners after which they have 3 minutes to pitch these to a jury of experts.

#### Motivation?
This solution is a part of the [case](https://github.com/START-Hack/UNCCD_STARTHACK24?tab=readme-ov-file) provided by G20 Global Land Initiative in cooperation with Universitat Politècnica de Catalunya which proposed a mission to come up with Tackling Wildfire Land degradation in Brazil.
#### Solution.
Forestify is an innovative platform designed to revolutionize wildfire prevention and management in Brazil. By leveraging the power of Geographic Information Systems (GIS), drones, and satellite technology, Forestify offers a comprehensive, integrated solution to mitigate wildfires' economic and environmental impacts, offering a mechanism for early wildfire detection.

The case provided consisted of the three following pillars:

 -  Enhance wildfire detection in Brazil using a deep-learning model
    
 -  Develop a platform that helps understand the extent of land degradation in Brazil using various datasets.
	 - A MODIS time series satellite imagery, covering Brazil to evaluate extent of burned areas (i.e. number of hectares, spatial distribution of the burned areas…)
	-   A MODIS landcover dataset to identify the type of land cover within the burn areas and assess the impact of different land cover types on the severity of wildfires.
	-   100m gridded population data to assess the impact on the population.
 -  Pitch an innovative Visualization solution for Land restoration to Brazilian Government representatives.
    

### 2. Features

-   For the first part of the project to improve the deep-learning model for wildfire detection in Brazil, our team used a combination of different data sets from various sources including wildfire image datasets we found on different research papers to improve and test the improved architecture of our deep-learning model. These datasets are linked in the references below. The deep-learning model is an EfficientNetB0 model trained on the ImageNet dataset for image classification. We then fine train all-but-the-first layer of this model on the three mentioned datasets using an 80-20 train-test split, an image size of 288x288 with 3 channels for color, a batch size of 32, and a learning rate of 0.001. We added two extra layers: a Global Average Pooling layer, and a dropout layer. The activation function for the output layer is sigmoid. We train using an Adam optimizer and Binary Cross Entropy loss function. The accuracy is close to **96%** on the initial test set given in the challenge.
    

Dynamic Dashboard

-   User-Friendly Interface: Additionally we have made a prototype of a user-friendly dashboard specifically tailored for the firefighting department administrators, enabling quick access between the GIS data analysis and soil-moisture sensor data for easy navigation and early detection. The web dashboard was created using Streamlit and the maps were created using the Google Earth Engine API.
    
-   Real-Time Data Visualization: Integrates data from various sources like soil moisture sensors, satellite imagery, and UAVs to provide a macroscopic view of forest health and micro-level data on dry regions.

### 3. Visuals
**Screenshots of the Dashboard that visualises the data:**

![Land Cover Changes of Years](https://github.com/daniel-sparemblek/starthack-g20/blob/main/images/viz6.png?raw=true)

![Dashboard](https://github.com/daniel-sparemblek/starthack-g20/blob/main/images/viz5.png?raw=true)

### 5. References and Research Literature
We investigated the problem thoroughly and thanks to depth-through research papers, we were able to obtain a more profound understanding of the problem, potential solutions and limitations, therefore, we want to reference those papers for further investigation into the problem. 

El-Madafri, I., Peña, M., & Olmedo-Torre, N. (2023). The Wildfire Dataset: Enhancing Deep Learning-Based Forest Fire Detection with a Diverse Evolving Open-Source Dataset Focused on Data Representativeness and a Novel Multi-Task Learning Approach. In Forests (Vol. 14, Issue 9, p. 1697). MDPI AG. https://doi.org/10.3390/f14091697

https://www.kaggle.com/datasets/elmadafri/the-wildfire-dataset
https://www.kaggle.com/datasets/alik05/forest-fire-dataset
https://www.kaggle.com/datasets/brsdincer/wildfire-detection-image-data



### 6. Contributors and Acknowledgment
It would not be possible to come up with this project within 36 hours during START Summit St. Gallen without our amazing team members and the mentors from G20 Global Land Initiative and 
-   Contributors: 
	- Mariam Abdallah - for the amazing data visualisations
	- Daniel Rey Sparemblek & Ali Tolga Dinçer - for the contributions in training and improving the deep-learning model
	- Milena Matevosyan - for packaging up a solution proposal for improved wildfire management
 
- Mentors we want to deliver our sincere thanks to:
	- Ismail El-Madafari
	- [Devashree Niraula](https://www.linkedin.com/in/devashree-niraula-1916a91b4/)


### 7. Contact Information

Reach out to us via email or LinkedIn if you have any further questions about the projects or if you would like to learn more from us:

- [Daniel Rey Sparemblek](https://www.linkedin.com/in/daniel-sparemblek/) - daniel.sparemblek@gmail.com
- [Ali Tolga Dinçer](https://www.linkedin.com/in/ali-tolga-dincer/) - alitolga.dincer@gmail.com
- [Mariam Abdallah](https://www.linkedin.com/in/mariam-abdallah-b46409224/)  - mariamabdallah4815@gmail.com
- [Milena Matevosyan](https://www.linkedin.com/in/milena-matevosyan/) - matevosyan.milena@gmail.com
