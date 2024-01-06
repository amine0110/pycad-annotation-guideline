# PYCAD Annotation Guidelines

This repository is dedicated to the web application from PYCAD, designed to expedite your annotation process. As highlighted, the application is not intended for diagnostic purposes and has not received `FDA` or `CE` approval. It assists in predicting an initial mask, which you can either use as-is or modify in 3D Slicer or your preferred annotation software. The final output can then be utilized for training your models.

https://github.com/amine0110/pycad-annotation-guideline/assets/37108394/1ae36158-ca83-4248-8084-24c8135df707

## How to Access the Application?
There are two versions of the application: a web version and a desktop version. The web version is currently live but is hosted on a non-GPU server. While it remains fast for inference, high traffic can occasionally lead to failures. To address this, we are developing a desktop version, which promises greater stability. This version can be run on your own machine, eliminating the need to upload sensitive datasets to a server. Additionally, please note that any dataset uploaded to the web application is not accessed or used in any way. We implement an automatic self-cleaning process every hour to delete all stored datasets.

Link to the web application: https://www.annotation.pycad.co/

## How to Use the Application?
The application is made to be user-friendly, so the process is very easy:
- Upload a zip file that contains DICOMs (the DICOM files should have the extension .dcm)
- Run the inference and wait (about a minute if there is not a lot of traffic)
- Visualize the 3D Output: Upon completion of the inference process, the output will be automatically displayed. You will have the ability to interact with the 3D mesh directly within the app
- Download the NIFTI output: Upon completion of the inference process, a button will be shown to give you the possibility to download the NIFTI file that contains the segmentation

## Information About the Models
The application is based 100% on Python, where the models were trained using YOLOv8 and the UI was built using Streamlit. Here are some information about the training and how to download the models checkpoints.

| Model        | N. Training Data | Data Modality | N. Epochs | mAP  (%) | Ckpts | Download Dataset |
|--------------|------------------|-----------|-------|-------|-------|-------|
| Lungs | 400  | CT | 22  | 95 | [Ckpt](https://drive.google.com/file/d/1NirjDsF_QhqfsB2ZtJO8bpH-PQ7YSGnk/view?usp=sharing) | Soon |
| Heart | 400  | CT | 120  | 89 | [Ckpt](https://drive.google.com/file/d/1DPY59bKAFZLvz7B5L00NeYBOJLRt6e7e/view?usp=sharing) | [Available](https://drive.google.com/file/d/1aqRAdbo70gngaQwuVsK9qi3cYjodiKmz/view?usp=sharing) |
| Liver | 400  | CT | 150  | 93 | [Ckpt](https://drive.google.com/file/d/1FOqPd9bIqXRynbDScBSoDFlDFm56SPsM/view?usp=sharing) | [Available](https://drive.google.com/file/d/15G11RYvOXoIF5rm-ya5rC4394-0hVxA6/view?usp=sharing) |
| Spleen | 400  | CT | 120  | 90 | [Ckpt](https://drive.google.com/file/d/1aNDXzbxIRHqMbpEDYa5VaIO4jRWzVg4b/view?usp=sharing) | [Available](https://drive.google.com/file/d/1cuPzACQH4l_VN5NZOyCCy9ElAu4SQ1-Q/view?usp=sharing) |
| Hips | 400  | CT | 145  | 99 | [Ckpt](https://drive.google.com/file/d/13_otIfYXWZWy477qTF2RniLXl1nS1Ui6/view?usp=sharing) | [Left](https://drive.google.com/file/d/1QwiMnlrwieT_Q0aatLb-Mh0wOLsbW4cq/view?usp=sharing), [Right](https://drive.google.com/file/d/1JBm_h6jKUvi0XAnyXusenZriQdG8lHLZ/view?usp=sharing) |
| Spine | 400  | CT | 74  | 92 | [Ckpt](https://drive.google.com/file/d/1YAZ6pAW6Q2Mh0rs0w0ivUpezdU1tZZNn/view?usp=sharing) | Soon |

## Feedback

We value your input and would love to hear your thoughts and suggestions! If you have any feedback about our models or the application, please feel free to share it with us. You can submit your feedback by creating a new issue in the [Issues](https://github.com/amine0110/pycad-annotation-guideline/issues) section of this repository. Your insights are important to us and will help improve the quality of our work.

---
<p align="center"> 
  You are the visitor number<br>
  <img src="https://profile-counter.glitch.me/amine0110%2Fpycad-annotation-guideline/count.svg" />
</p>
