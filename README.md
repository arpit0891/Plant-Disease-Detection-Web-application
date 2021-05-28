## About Plant Disease Detection Web Application
   - Deep learning with convolutional neural networks (CNNs) has achieved great success in the classification of various plant diseases. However, a limited number of studies have elucidated the process of inference, leaving it as an untouchable black box. 
   - Revealing the CNN to extract the learned feature as an interpretable form not only ensures its reliability but also enables the validation of the model authenticity and the training dataset by human intervention. 
   - In this study, a variety of neuron-wise and layer-wise visualization methods were applied using a CNN, trained with a publicly available plant disease image dataset. We showed that neural networks can capture the colors and textures of lesions specific to respective diseases upon diagnosis, which resembles human decision-making. 
   - While several visualization methods were used as they are, others had to be optimized to target a specific layer that fully captures the features to generate consequential outputs. Moreover, by interpreting the generated attention maps, we identified several layers that were not contributing to inference and removed such layers inside the network, decreasing the number of parameters by 75% without affecting the classification accuracy. 
   - The results provide an impetus for the CNN black box users in the field of plant science to better understand the diagnosis process and lead to further efficient use of deep learning for plant disease diagnosis.
   
 Motive---->>>
For this challenge, I used the “PlanVillage” dataset. This dataset contains an open access repository of images on plant health to enable the development of mobile disease diagnostics. The dataset contains 54, 309 images. The images span 14 crop species: Apple, Blueberry, Cherry, Grape, Orange, Peach, Bell Pepper, Potato, Raspberry, Soybean, Squash, Strawberry, and Tomato. It contains images of 17 fundal diseases, 4 bacterial diseases, 2 molds (oomycete) diseases, 2 viral diseases, and 1 disease caused by a mite. 12 crop species also have images of healthy leaves that are not visibly affected by a disease.
   **Go to https://spj.sciencemag.org/plantphenomics/2019/9237136/ to read the complete article about 'How Convolutional Neural Networks Diagnose Plant Disease'**
 


## Server Set-Up  (For Training)
- **Google Cloud Platform (Intermediate)** - The complete tutorial can be found [*here*](https://course.fast.ai/start_gcp.html)

- **Gradient (Easy)** -  The complete tutorial can be found [*here*](https://course.fast.ai/start_gradient.html)

- **AWS EC2 (Advance)** - The complete tutorial can be found [*here*](https://course.fast.ai/start_aws.html)
```
git clone https://github.com/arpit0891/Plant-Disease-Detection-Web-application.git

cd ./Plant-Disease-Detection-Web-application/'Web Application'

docker build -t fastai-v3

docker run --rm -it -p 8080:8080 fastai-v3
```
## Dataset Description:

|Name           | No of Classes | Class Names
| ------------- |:-------------:|:-----------------:|
| Apple     |     04        | 'Apple___Apple_scab','Apple___Black_rot','Apple___Cedar_apple_rust' 'Apple___healthy' |
| Blueberry |     01        | 'Blueberry___healthy' |
| Cherry    |     02        | 'Cherry_(including_sour)_Powdery_mildew', 'Cherry_(including_sour)_healthy' |
| Corn      |     04        | 'Corn___Cercospora_leaf_spot', 'Corn___Common_rust','Corn___Northern_Leaf_Blight','Corn___healthy' |
| Grape     |     04        | 'Grape___Black_rot','Grape___Esca_(Black_Measles)','Leaf_blight_(Isariopsis_Leaf_Spot)','Grape___healthy' |
| Orange    |     01        | 'Orange___Haunglongbing_(Citrus_greening)' |
| Peach     |     02        | 'Peach___Bacterial_spot','Peach___healthy' |
| Pepper    |     02        | 'Pepper,_bell___Bacterial_spot','Pepper,_bell___healthy' |
| Potato    |     03        | 'Potato___Early_blight','Potato___Late_blight','Potato___healthy' |
| Raspberry |     01        | 'Raspberry___healthy' |
| Soyabean  |     01        | 'Soybean___healthy' |
| Squash    |     01        | 'Squash___Powdery_mildew' |
| Strawberry|     02        | 'Strawberry___Leaf_scorch','Strawberry___healthy' |
| Tomato    |     10        | Tomato: 'Bacterial_spot','Early_blight', 'Late_blight', 'Leaf_Mold', 'Septoria_leaf_spot', 'Spider_mites','Target_Spot', 'Yellow_Leaf_Curl_Virus', 'Mosaic_virus', 'Healthy' |
