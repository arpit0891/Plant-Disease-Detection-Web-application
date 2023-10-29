## About The Plant Disease Detection Web Application

This web application leverages AI to identify diseases in plants, utilizing the FastAI library built atop Facebook's deep learning platform, PyTorch. It employs an open-access dataset repository for training and validation purposes.

Automated plant disease detection eases the substantial workload entailed in monitoring large agricultural expanses. The application is designed to identify symptoms at an early stage when they manifest on plant foliage.

### Motivation

The initiative for this project was drawn from the "PlanVillage" dataset, encompassing an open-access image repository aimed at advancing mobile disease diagnostic solutions for plants. The dataset aggregates 54,309 images across 14 crop species, including but not limited to Apple, Blueberry, and Tomato. It's a rich resource illustrating 17 fungal diseases, 4 bacterial diseases, 2 mold (oomycete) diseases, 2 viral diseases, and 1 mite-induced disease. Additionally, images of healthy leaves from 12 crop species are included to provide a comprehensive view.

![Demo GIF](https://github.com/arpit0891/Plant-Disease-Detection-Web-application/blob/master/pdd.gif)

![App Interface](https://github.com/arpit0891/Plant-Disease-Detection-Web-application/blob/master/pdd.png)

### Technical Insights

- Utilizing Convolutional Neural Networks (CNNs) for deep learning has significantly enhanced the classification accuracy of various plant diseases. However, the lack of insight into the underlying inference process leaves it dubbed as a "black box."
- This study aims to demystify the CNN by extracting and visualizing learned features in an interpretable manner, thereby ensuring model reliability and enabling human validation of the model and dataset.
- A host of neuron-wise and layer-wise visualization methods were employed on a CNN trained with a publicly available plant disease image dataset. The findings reveal that neural networks effectively discern the color and texture of lesions characteristic of specific diseases, mirroring human diagnostic procedures.
- A variety of visualization methods were optimized to target specific layers that fully capture consequential features. By interpreting the generated attention maps, several non-contributory layers were identified and eliminated from the network, reducing the parameter count by 75% without compromising classification accuracy.
- The outcomes of this study encourage a broader understanding and more efficient deployment of deep learning for plant disease diagnosis within the plant science community.

For a deeper dive into the study, visit [How Convolutional Neural Networks Diagnose Plant Disease](https://spj.sciencemag.org/plantphenomics/2019/9237136/).

### Server Set-Up (For Training)

- **Google Cloud Platform (Intermediate)** - Complete tutorial available [here](https://course.fast.ai/start_gcp.html).
- **Gradient (Easy)** - Complete tutorial available [here](https://course.fast.ai/start_gradient.html).
- **AWS EC2 (Advanced)** - Complete tutorial available [here](https://course.fast.ai/start_aws.html).

```bash
git clone https://github.com/arpit0891/Plant-Disease-Detection-Web-application.git
cd ./Plant-Disease-Detection-Web-application/'Web application'
sudo pip install -r requirements.txt
sudo docker build -t pdd .
sudo docker images --filter reference=pdd
sudo docker run -t -i -p 8080:8080 pdd
```

## Dataset Description:

| Name       | No of Classes |                                                                                 Class Names                                                                                  |
| ---------- | :-----------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| Apple      |      04       |                                            'Apple**_Apple_scab','Apple_**Black_rot','Apple**_Cedar_apple_rust' 'Apple_**healthy'                                             |
| Blueberry  |      01       |                                                                           'Blueberry\_\_\_healthy'                                                                           |
| Cherry     |      02       |                                                'Cherry*(including_sour)\_Powdery_mildew', 'Cherry*(including_sour)\_healthy'                                                 |
| Corn       |      04       |                                      'Corn**_Cercospora_leaf_spot', 'Corn_**Common_rust','Corn**_Northern_Leaf_Blight','Corn_**healthy'                                      |
| Grape      |      04       |                                 'Grape**_Black_rot','Grape_**Esca*(Black_Measles)','Leaf_blight*(Isariopsis_Leaf_Spot)','Grape\_\_\_healthy'                                 |
| Orange     |      01       |                                                                 'Orange*\_\_Haunglongbing*(Citrus_greening)'                                                                 |
| Peach      |      02       |                                                                  'Peach**_Bacterial_spot','Peach_**healthy'                                                                  |
| Pepper     |      02       |                                                          'Pepper,\_bell**_Bacterial_spot','Pepper,\_bell_**healthy'                                                          |
| Potato     |      03       |                                                     'Potato**_Early_blight','Potato_**Late_blight','Potato\_\_\_healthy'                                                     |
| Raspberry  |      01       |                                                                           'Raspberry\_\_\_healthy'                                                                           |
| Soyabean   |      01       |                                                                            'Soybean\_\_\_healthy'                                                                            |
| Squash     |      01       |                                                                         'Squash\_\_\_Powdery_mildew'                                                                         |
| Strawberry |      02       |                                                              'Strawberry**_Leaf_scorch','Strawberry_**healthy'                                                               |
| Tomato     |      10       | Tomato: 'Bacterial_spot','Early_blight', 'Late_blight', 'Leaf_Mold', 'Septoria_leaf_spot', 'Spider_mites','Target_Spot', 'Yellow_Leaf_Curl_Virus', 'Mosaic_virus', 'Healthy' |
