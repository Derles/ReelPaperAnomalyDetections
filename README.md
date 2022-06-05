
# Reel paper anomaly detections

The aim of the project is to create a mechanism for detecting paper defects on the splicer of a web press in order to minimize the risk of the paper breaking. The solution will be based on paper anomaly detection based on image recognition.


## Table of Contents


 1. [Web Offset Printing Overview](#web-offset-printing-overview)
 2. [Web Breaks Problems In Offset Printing](#web-breaks-problems-in-offsetrinting)
 3. [Project Phases](#project-phases)  
    3.1 [Identification and description of the problem](#identification-and-description-of-the-problem)  
    3.2 [Data collection](#data-collection)  
    3.3 [Categorization of samples](#categorization-of-samples)  
    3.4 [Overview of existing solutions](#overview-of-existing-solutions)   
    3.5 [Implementing own solution](#implementing-own-solution)
 4. [References](#references)


### Web Offset Printing Overview

Web offset is a form of offset printing in which a continuous roll of paper is fed through the printing press. Pages are separated and cut to size after they have been printed. Web offset printing is used for high-volume publications such as mass-market books, magazines, newspapers, catalogs and brochures

Figure below shows printing flow and general concept of web ofset press.

  ![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Web-offset-press-components.jpg?raw=true)

The first element of the flow is a Reel Stand/Reel Splicer wchich main task are unwind the paper reel, tension the paper web and keep it at constant tension and
change the reel fully automatically.

The simplest version of a printing unit is the vertical blanket-to-blanket one which uses a horizontal web-lead to print one color on the front and reverse side of the web; this is standard in web offset printing.
 The printing section is composed of two printing couples arranged in tandem as shown on a figure below.

 ![Screenshot](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Blanket-to-blanket-printing-unit-of-a-web-offset-printing-press.jpg?raw=true)

 ### Web Breaks Problems In Offset Printing

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
[![Web breaks example 1](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Web-breaks-example1.jpg?raw=true)](https://youtu.be/p3pbLeURK8Q?t=72s "Web breaks example 1")

#### Web break example #2
[![Web breaks example 2](https://github.com/Derles/ReelPaperAnomalyDetections/blob/main/Images/Web-breaks-example2.jpg?raw=true)](https://youtu.be/0fFKKYjYvJI?t=135s "Web breaks example 1")


### Project Phases

#### Identification and description of the problem

Opisać problem zrywu papieru, jaka jest teraz skala i jak to jest teraz robione

#### Data collection

Opisać, że aktualnie zbierane są dane z czterech maszyn rolowych

#### Categorization of samples

Opisać jakie kategorie wad występują, które są dominujące - podać przykłady:

- [Faktura Papieru]
- [Defekty powłoki]
- [Pęknięcie brzegowe]
- [Dziura]
- [Klejenie fabryczne]
- [Uszkodzenie transportowe]
- [Zmarszczki]

Przygotowanie zestawów zawierających po 300 zdjęć z każdej kategori, próba rozszerzenia próbki do 1500 zdjęć na kategorię.
Próba zbalansowania próbek na kategorię

#### Overview of existing solutions



#### Implementing own solution

Stworzenie rozwiązania opartego o bibliotekę opencv, które umożliwi rozpoznawanie 5 najczęstrzych kategorii wad. Na ten moment skupiam się na kategori dotyczącej dziur

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

## Authors

- [@Derles](https://github.com/Derles)


## Roadmap

- Additional browser support

- Add more integrations

