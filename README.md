## README

In this file, we will explain how to reproduce the results we obtained for our project. <br> 
To reproduce our results, download the pretrained model for the result you want to reproduce from the "Pretrained models from report" section in this file. Reference this downloaded checkpoint file in Inference.ipynb in the cell defining the model_array used. <br>
Additionally, you must download the data used when training the aforementioned model, through the relevant link under the "Data" section in this file. This includes both the images, and the associated csv file. <br>
The path to the downloaded images must be referenced in TRAIN_DATA_FOLDER in Inference.ipynb, and the csv file must be referenced where the data_df variable is defined in Inference.ipynb. <br>
Furthermore, the hotel-code mapping must be downloaded through the link defined under 'Hotel-code mapping used in Training.ipynb and Inference.ipynb'. <br>
This downloaded mapping should be referenced in the Inference.ipynb where hotel_id_code_df is defined. <br>
This Inference.ipynb notebook should be committed on Kaggle, and the committed notebook must be submitted on Kaggle.

## Notebooks

All notebooks used during the project are stored in the 'notebooks' folder. 
This folder includes the following notebooks:

 - Preprocessing.ipynb, used to preprocess the images from Kaggle. It is altered to our needs from: https://www.kaggle.com/code/michaln/hotel-id-image-preprocessing-256x256
 - Hotels-50K.ipynb, used to download Hotels-50k images and preprocess them. It is altered to our needs from: https://www.kaggle.com/code/michaln/hotels-50k-eda-and-image-download
 - Duplicate_files_removal.ipynb, used to remove duplicate files present in the data. It is altered to our needs from: https://medium.com/analytics-vidhya/removing-duplicate-docs-using-parallel-processing-in-python-53ade653090f
 - Training.ipynb, used to train models. It is altered to our needs from: https://www.kaggle.com/code/michaln/hotel-id-arcmargin-training
 - Inference.ipynb, used to create the submission file for Kaggle. It is altered to our needs from: https://www.kaggle.com/code/michaln/hotel-id-inference
 - Baseline.ipynb, used for our first submission.

## Data
Hotel-ID 256x256: <br>
https://www.kaggle.com/datasets/michaln/hotelid-2022-train-images-256x256 <br>
Hotel-ID 512x512: <br>
https://www.kaggle.com/datasets/michaln/hotelid-2022-train-images-512x512 <br>
Hotel-ID + Hotels-50K 256x256: <br>
www.kaggle.com/dataset/f11ae8dcb0102afcbcd1a26e0b685639ee63cb2f6c0ec97d2415b566b6086811 <br>
Hotel-ID + Hotels-50K 512x512: <br>
www.kaggle.com/dataset/5e37ed466300424b56e448ebc20109e6887dece46e43f6fccb8de71a21e0bcf3 <br>

Unfortunately, the other image sizes used in the image size experiment are not available anymore.
You can create this data by running the Preprocessing.ipynb notebook, with the respective image size you want the data to
have selected.

## Csv files used in Training.ipynb and Inference.ipynb:
Hotel-ID 256x256: <br>
https://www.kaggle.com/datasets/michaln/hotelid-2022-train-images-256x256 (see train.csv) <br>
Hotel-ID 512x512: <br>
https://www.kaggle.com/datasets/michaln/hotelid-2022-train-images-512x512 (see train.csv) <br>
Hotel-ID + Hotels-50K 256x256: <br>
www.kaggle.com/dataset/abcce9f5e927583f3353113f1dc843c296f119146f009b4101b43716e3919a47 <br>
Hotel-ID + Hotels-50K 512x512: <br>
www.kaggle.com/dataset/a7055ae0e77048520a613b9144ab56fb2e92f99bc366dadbd2a7b68177bba7b8 <br>

## Hotel-code mapping used in Training.ipynb and Inference.ipynb
www.kaggle.com/dataset/94d769fd054d7c50d49835bb6933db2d3ddba45b35567b24bd5ab17c29402678

## Pretrained models from report

#### ArcFace
ArcFace: <br>
www.kaggle.com/dataset/ef9f3a4f2f282d6b6ac28205bb07a0845cd16cf79b3adf3e756923b0002f4fdf <br>
CE-Loss: <br>
www.kaggle.com/dataset/56401e30357bf3b8a6c4c6926ed62cf908c951193c9be2d6a77a71f23aeb6904 <br>

#### Backbone
efficientnet_b0: <br>
www.kaggle.com/dataset/ef9f3a4f2f282d6b6ac28205bb07a0845cd16cf79b3adf3e756923b0002f4fdf <br>
eca_nfnet_l0: <br>
www.kaggle.com/dataset/a77c977bbef5f83e0311938efe1c8d055b8b388165e6e387ca654f889a3e7e83 <br>
nfnet_l0: <br>
www.kaggle.com/dataset/3900e4d41d1e26ddf4730d5abbd014ed65d762aa612ed60debe23f7a3b7c562b <br>

#### Image size
256x256: <br>
www.kaggle.com/dataset/a77c977bbef5f83e0311938efe1c8d055b8b388165e6e387ca654f889a3e7e83 <br>
672x672: <br>
www.kaggle.com/dataset/1299d745c8185f0f0fd29302fa3daa9c32a73eebe9f8bea5cf5141afcc18ac11 <br>

Unfortunately, the other pretrained models from this experiment were removed to save disk space and are not available anymore. You can reproduce these results, by using Preprocessing.ipynb to create the dataset with the respective image size you want the data to have. Afterwards, you can train the model on this dataset for 3 epochs with the eca_nfnet_l0 model using the Training.ipynb notebook. The resulting checkpoint file should correspond to our pretrained models used.

#### Ensemble

Best performing single model: <br>
www.kaggle.com/datasets/30e9e81a3abc85667889ea6f69f3a141f3cf38952510dfa6c6ab5c929792b8f7 <br>

Bagging with 5 eca_nfnet_l0 models: <br>
www.kaggle.com/dataset/aefdb59004a27357e37f0fa6fdd894e22ed26bebe6b50e65a494fd4a81362fa1 <br>
www.kaggle.com/dataset/2a8fa7b5522f463a9cd4866956a0d1bea127d1d603afc3f9ef5b28052841487e <br>
www.kaggle.com/dataset/17f86071bcfba2c2ca95509be506a5bb7987ac5063cff101d35623e4d3270a8d <br>
www.kaggle.com/dataset/fd787ef33e44e3b397b8ad8187779d9dfca9759a0a1a40ca58b9dea4e6715fd7 <br>
www.kaggle.com/dataset/0759f5ef919860f3d75e3600953b849b5b935528b7aa5b8e95cb316a420d4268 <br>

Heterogeneous ensemble: <br>
www.kaggle.com/datasets/30e9e81a3abc85667889ea6f69f3a141f3cf38952510dfa6c6ab5c929792b8f7 <br>
www.kaggle.com/dataset/ff7ed63726e7b9b2ff7d03984923ad7cfb53a88196306e22503a13962df22243  <br>

Bagging with 3 eca_nfnet_l0 models + heterogeneous ensemble <br>
www.kaggle.com/datasets/30e9e81a3abc85667889ea6f69f3a141f3cf38952510dfa6c6ab5c929792b8f7 <br>
www.kaggle.com/dataset/ff7ed63726e7b9b2ff7d03984923ad7cfb53a88196306e22503a13962df22243 <br>
www.kaggle.com/dataset/0759f5ef919860f3d75e3600953b849b5b935528b7aa5b8e95cb316a420d4268 <br>
www.kaggle.com/dataset/fd787ef33e44e3b397b8ad8187779d9dfca9759a0a1a40ca58b9dea4e6715fd7 <br>
www.kaggle.com/dataset/17f86071bcfba2c2ca95509be506a5bb7987ac5063cff101d35623e4d3270a8d <br>


