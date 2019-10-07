# De-Identification of medical images using AWS
In this post we will learn how to use AWS Services to de-identify medical inages before making them eligible for medical imaging. 

Medical Imaging is the most intanglible element in medical practice in this day and age. Thanks to modern medical imaging modalities, practitioners and scientists can learn more about the human body than ever before. However, most of the medical imaging modalities have .dicom images and also contain information which can be traced back to the patient thereby making these images useless for further processing and research. 

Hence, it is imperative for researchers to come out with tools which would help make these images accessible to the wider medical community using the AI services of AWS. 

The pipeline would look something like this - 
1) Upload images to S3. 
2) Read images into Amazon Sagemaker. 
3) Change the format of the images from 'Dicom' to 'jpeg'. 
4) Run Amazon Rekognition on top of it to identify the text. 
5) Pass on the text through Amazon Comprehend Medical to identify if it contains any Personal Health Information (PHI). 
6) Redact the PHI using OpenCV and then make it available to the broader medical community for research purposes. 
