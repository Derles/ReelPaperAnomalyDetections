
# Reel paper anomaly detections

The aim of the project is to create a mechanism for detecting paper defects on the splicer of a web press in order to minimize the risk of the paper breaking. The solution will be based on classification  whether an input image of paper web (image recognition) contains anomalies or not.


## Table of Contents


 1. [Web offset printing overview](#web-offset-printing-overview)
 2. [Web breaks problems on offset printing](#web-breaks-problems-in-offsetrinting)
 3. [Project phases](#project-phases)  
    3.1 [Identification and description of the problem](#identification-and-description-of-the-problem)  
    3.2 [Data collection](#data-collection)  
    3.3 [Categorization of samples](#categorization-of-samples)  
    - [Texture of paper](#texture-of-paper)
    - [Shell defects](#shell-defects)
    - [Edge cracks](#edge-crack)
    - [Holes](#holes)
    - [Factory gluing](#factory-gluing)
    - [Transport damages](#transport-damages)
    - [Wrinkles](#wrinkles)
    
    3.4 [Overview of existing solutions](#overview-of-existing-solutions)   
    3.5 [Implementing own solution](#implementing-own-solution)
 4. [References](#references)


### Web offset printing overview

Web offset is a form of offset printing in which a continuous roll of paper is fed through the printing press. Pages are separated and cut to size after they have been printed. Web offset printing is used for high-volume publications such as mass-market books, magazines, newspapers, catalogs and brochures

Figure below shows printing flow and general concept of web offset press.

  ![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Web-offset-press-components.jpg?raw=true)

The first element of the flow is a Reel Stand/Reel Splicer which main task are unwind the paper reel, tension the paper web and keep it at constant tension and
change the reel fully automatically.

The simplest version of a printing unit is the vertical blanket-to-blanket one which uses a horizontal web-lead to print one color on the front and reverse side of the web; this is standard in web offset printing.
The printing section is composed of two printing couples arranged in tandem as shown on a figure below.

 ![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Blanket-to-blanket-printing-unit-of-a-web-offset-printing-press.jpg?raw=true)

Standard web press has four printing units for main inks CMYK (Cyan, Magenta, Yelow and Black).

At the end of the printing process paper web is folded and cut into signatures.
 
### Web breaks problems in offset printing

Runnability is defined as a printing process without any faults, interruptions, and stops. Web breaks,
web instability, register errors and wrinkling are examples for runnability
problems which affect productivity and also the quality of the products, and
cause huge losses.

Web breaks are considered as the most significant cause of runnability
problems. Web breaks occur when the total applied load on the web exceeds
the strength of the web. There are two main factors affecting the occurrence
of web breaks: the applied load and the web strength. Both factors vary
randomly around a mean value from time to time. There are different sources
causing the variation in the applied load and the web strength.

#### Web break example #1
On this video the hole in the paper (starts about 1:10m) causes paper break (1:54m)
[![Web breaks example 1](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Web-breaks-example1.jpg?raw=true)](https://youtu.be/p3pbLeURK8Q?t=70s "Web breaks example 1")

#### Web break example #2
[![Web breaks example 2](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Web-breaks-example2.jpg?raw=true)](https://youtu.be/0fFKKYjYvJI?t=135s "Web breaks example 1")

#### Web break example #3
On this video the paper anomaly of edge crack (starts at 10s) causes paper break (about 2:30m)
[![Web breaks example 3](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Web-breaks-example3.jpg?raw=true)](https://youtu.be/-D4jnl8v4jk?t=10s "Web breaks example 1")



### Project phases

#### Identification and description of the problem

The problem of paper breaks on web presses is one of the most onerous problems in ensuring a continuous and trouble-free printing process. The paper is the most expensive raw material in the printing process and each breakage generates additional costs related to the material as well as machine downtime.
Early detection of a paper defect, which with a high degree of probability will result in paper breakage, can significantly reduce the costs related to the occurrence of breaks or even prevent them earlier.
The lack of a system detecting anomalies of the reel paper means that at this point the situation comes down to the post factum assessment (after the paper break) whether it is related to a defect of the manufacturer's paper. After the occurrence of such an event, the employee manually analyzes hundreds of images from the reel stand/reel splicer to assess whether the break was due to a defect of the paper manufacturer, then a complaint is prepared with the appropriate evidence material.
The introduction of the image recognition mechanism on the web press unwinder and then the recognition of labeled defect categories, such as e.g. holes, not only could protect against potential breaks of paper, but also automate the complaint process.
The proposed solution would analyze images from the reel stand/reel splicer of web press and if a given image was classified as one of the anomalies, it would alert the machine operator who would take further actions, including stopping the printing.

Stage status: Done

#### Data collection

At the moment, data on complaints related to the breaks of paper for the current and last year have been collected from four different web presses from two independent locations.

Stage status: First data samples already collected, it is continuous process.

#### Categorization of samples

The following seven defect categories presented below were distinguished in the process related to the filing of complaints regarding the tear of paper. The dominant category seems to be the category related to the presence of holes in the reel paper.

Samples are stored in sub-folder: Samples

Stage status: Done

##### Texture of paper
The example of the paper anomaly related with paper texture's:
  ![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Texture-of-paper-exemple1.jpg?raw=true)

##### Shell defects
The example of the shell defect on a paper reel:
  ![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Shell-defects-example1.jpg?raw=true)

##### Edge crack
The edge crack example:
![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Edge-crack-example1.jpg?raw=true)

##### Holes
The example of paper anomaly caused by holes:
![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Hole-example1.jpg?raw=true)

##### Factory gluing
The example of the factory gluing defect:
![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Factory-gluing-example1.jpg?raw=true)

##### Transport damages
Anomalies caused during transportation:
![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Transport-damages-example1.jpg?raw=true)

##### Wrinkles
The examples of wrinkles:
![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Wrinkles-example1.jpg?raw=true)


A further goal in this phase of the project is to prepare well-balanced samples of a minimum of 300 images for each anomaly category, then try to expand these samples to around 1500 images. At the moment, it is already known that it will not be easy to achieve due to the availability of collected complaint materials and the quality of the images (the main problem is lighting).
The category related to the holes in the reel paper appears to be the best documented, therefore further work will mainly focus on this category of defects. If sufficient samples are obtained for the remaining defect categories, further work on them will also be carried out.

Stage status: Partly done, still in progress

#### Overview of existing solutions

Stage status: Partly done, still in progress

#### Implementing own solution

At this stage of the project, based on the OpenCV (Open Source Computer Vision Library: http://opencv.org), a solution is created to recognize anomalies related to the occurrence of the holes on the paper web on reel stand/reel splicer of web press.

At the next step I would like to build a machine learning model which is able to classify whether an input image of reel paper contains anomalies or not.
I decided to use VGG16 a Convolutional Neural Network (CNN) model proposed by Karen Simonyan and Andrew Zisserman which seems to be easy to implement in Keras.

Stage status: In progress

### References

- [https://towardsdatascience.com/anomaly-detection-in-images-777534980aeb](https://towardsdatascience.com/anomaly-detection-in-images-777534980aeb)
- [https://github.com/cerlymarco/MEDIUM_NoteBook/blob/master/Anomaly_Detection_Image/Anomaly_Detection_Image.ipynb](https://github.com/cerlymarco/MEDIUM_NoteBook/blob/master/Anomaly_Detection_Image/Anomaly_Detection_Image.ipynb)
- [https://towardsdatascience.com/anomaly-detection-in-images-777534980aeb?gi=eb073b267f97](https://towardsdatascience.com/anomaly-detection-in-images-777534980aeb?gi=eb073b267f97)
- [https://www.tensorflow.org/api_docs/python/tf/keras/applications](https://www.tensorflow.org/api_docs/python/tf/keras/applications)
- [https://medium.com/swlh/logistic-regression-for-image-classification-e15d0ae59ce9](https://medium.com/swlh/logistic-regression-for-image-classification-e15d0ae59ce9)
- [https://print-media-technology.blogspot.com/](https://print-media-technology.blogspot.com/)
- [http://m.wan-ifra.org/sites/default/files/field_article_file/EN%20WOCG%20Web%20Breaks_0.pdf](http://m.wan-ifra.org/sites/default/files/field_article_file/EN%20WOCG%20Web%20Breaks_0.pdf)
- [https://blog.mps-printing.com/](https://blog.mps-printing.com/)
- [http://offsetpressman.blogspot.com/](http://offsetpressman.blogspot.com/)
- [https://towardsdatascience.com/anomaly-detection-in-images-777534980aeb](https://towardsdatascience.com/anomaly-detection-in-images-777534980aeb)
- [https://keras.io/api/applications/vgg/](https://keras.io/api/applications/vgg/)
- [https://www.mygreatlearning.com/blog/introduction-to-vgg16/](https://www.mygreatlearning.com/blog/introduction-to-vgg16/)
- [https://neurohive.io/en/popular-networks/vgg16/](https://neurohive.io/en/popular-networks/vgg16/)

## Authors

- [@Derles](https://github.com/Derles)




