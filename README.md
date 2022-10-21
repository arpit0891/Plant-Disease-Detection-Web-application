## About Plant Disease Detection Web Application

AI web application that detects diseases in plants using FastAi which is built on the
top of Facebook’s deep learning platform: PyTorch.
The application uses open access repository for the dataset.

Detection of plant disease through some automatic technique is beneficial as it requires a large
amount of work of monitoring in big farm of crops, and at very early stage itself it detects symptoms of
diseases means where they appear on plant leaves.
Motive

For this challenge, I used the “PlanVillage” dataset. This dataset contains an open access repository of images on plant health to enable the development of mobile disease diagnostics. The dataset contains 54, 309 images. The images span 14 crop species: Apple, Blueberry, Cherry, Grape, Orange, Peach, Bell Pepper, Potato, Raspberry, Soybean, Squash, Strawberry, and Tomato. It contains images of 17 fundal diseases, 4 bacterial diseases, 2 molds (oomycete) diseases, 2 viral diseases, and 1 disease caused by a mite. 12 crop species also have images of healthy leaves that are not visibly affected by a disease.

![MOCK](https://github.com/arpit0891/Plant-Disease-Detection-Web-application/blob/master/pdd.gif)

![PDD](https://github.com/arpit0891/Plant-Disease-Detection-Web-application/blob/master/pdd.png)

- Deep learning with convolutional neural networks (CNNs) has achieved great success in the classification of various plant diseases. However, a limited number of studies have elucidated the process of inference, leaving it as an untouchable black box.
- Revealing the CNN to extract the learned feature as an interpretable form not only ensures its reliability but also enables the validation of the model authenticity and the training dataset by human intervention.
- In this study, a variety of neuron-wise and layer-wise visualization methods were applied using a CNN, trained with a publicly available plant disease image dataset. We showed that neural networks can capture the colors and textures of lesions specific to respective diseases upon diagnosis, which resembles human decision-making.
- While several visualization methods were used as they are, others had to be optimized to target a specific layer that fully captures the features to generate consequential outputs. Moreover, by interpreting the generated attention maps, we identified several layers that were not contributing to inference and removed such layers inside the network, decreasing the number of parameters by 75% without affecting the classification accuracy.
- The results provide an impetus for the CNN black box users in the field of plant science to better understand the diagnosis process and lead to further efficient use of deep learning for plant disease diagnosis.

Motive---->>>
For this challenge, I used the “PlanVillage” dataset. This dataset contains an open access repository of images on plant health to enable the development of mobile disease diagnostics. The dataset contains 54, 309 images. The images span 14 crop species: Apple, Blueberry, Cherry, Grape, Orange, Peach, Bell Pepper, Potato, Raspberry, Soybean, Squash, Strawberry, and Tomato. It contains images of 17 fundal diseases, 4 bacterial diseases, 2 molds (oomycete) diseases, 2 viral diseases, and 1 disease caused by a mite. 12 crop species also have images of healthy leaves that are not visibly affected by a disease.
**Go to https://spj.sciencemag.org/plantphenomics/2019/9237136/ to read the complete article about 'How Convolutional Neural Networks Diagnose Plant Disease'**

## Server Set-Up (For Training)

- **Google Cloud Platform (Intermediate)** - The complete tutorial can be found [_here_](https://course.fast.ai/start_gcp.html)

- **Gradient (Easy)** - The complete tutorial can be found [_here_](https://course.fast.ai/start_gradient.html)

- **AWS EC2 (Advance)** - The complete tutorial can be found [_here_](https://course.fast.ai/start_aws.html)

```
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
