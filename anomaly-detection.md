<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-R226D9G6FD"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-R226D9G6FD');
</script>

# CS Graduate Capstone Project: Network Anomaly Detection

## Background
The world of technology has allowed us to be more connected, but it also makes us more vulnerable to cyber threats. 
This makes advanced threat detection more important than ever. Our project builds on recent work by Carrera et al. [1], 
further testing their two-phase anomaly detection process. This process proposes that a model which predicts quickly 
can be used to reduce the incoming data load for a second, slower, more accurate model, thereby achieving faster and 
more accurate predictions than either model alone.

## Project Description
Our project investigated the pipelining of network traffic anomaly detection models to improve speed and accuracy over 
their components. We chose the NSL_KDD dataset, which contains packet data for network analysis and is meant as a train 
and test dataset for use in anomaly detection. The non-anomalous training data was preprocessed with a robust autoencoder [2]. 
We used autoencoder variants for the first phase and isolation forest variants for the second phase, including Isolation Forest [3], 
Extended Isolation Forest (EIF) [4], SCiForest (SCiF) [5], and Finite-Boundary Isolation Forest (FBiF) [6].

## Collaboration
Our project involved a group of me and two other students, along with our advisor. We worked together in class, and 
asynchronously, outside of class, meeting in class twice a week, and out of class once a week. 

## Tools and Technologies
The tools and technologies used in this project include:


- Autoencoders
<br>
- Isolation Forest variants
  - Isolation Forest
  - EIF
  - SCiF
  - FBiF
  
- Python
  - Tensorflow
  - Scikit-Learn
  - Numpy
  - Numba
  - Matplotlib
  - Pandas
<br>
<br>
#### Prediction speed comparison between each model

| Model                            | Predict Speed (Complete Test Set) |
|----------------------------------|-----------------------------------|
| Autoencoder                      | 0.031 seconds                     |
| Isolation Forest                 | 9.21 seconds                      |
| Extended Isolation Forest        | 15.8 seconds                      |
| SCiForest                        | 53.8 seconds                      |
| Finite Boundary Isolation Forest | 59.3 seconds                      |

<br>

#### Scores comparison between individual models (first 2 rows), along with pipeline tests (last 4 rows)

| Model Type             | Precision | Recall | F1    |
|------------------------|-----------|--------|-------|
| Autoencoder            | 0.46      | 0.51   | 0.49  |
| Isolation Forest       | 0.907     | 0.746  | 0.818 |
| AE -> Isolation Forest | 0.96      | 0.56   | 0.71  |
| AE -> Extended IF      | 0.83      | 0.36   | 0.50  |
| AE -> SCiForest        | 0.76      | 0.46   | 0.57  |
| AE -> FBIF             | 0.58      | 0.44   | 0.50  |

## Outcomes
The methodology used leads to significant time savings compared to using an isolation forest alone, but still has room
to further improve the scores in the phase-1 autoencoder. The potential for such improvement is
shown to potentially lie in underlying qualities of the autoencoder that are not yet well examined. Through this project,
I gained a deeper understanding of machine learning models and how to evaluate them effectively, using multiple metrics.
I also learned about network traffic data, and how to incorporate such data into ML models.

Our paper was published by IEEE and presented at IEEE CCWC 2024. <a href="https://ieeexplore.ieee.org/abstract/document/10427699">Link here</a>


<br><br>

<figure>
<a href="images/pipeline.jpg?raw=true" target="_blank">
<img src="images/pipeline.jpg?raw=true" alt="Example of the pipeline we used"/>
</a>
<figcaption>2-phase pipeline that we used. Image originally from [1].</figcaption>
</figure>


## References
[1]: Carrera, Francesco, et al. "Combining unsupervised approaches for near real-time network traffic anomaly detection." Applied Sciences 12.3 (2022): 1759.

[2]: Zong, Bo, et al. "Deep autoencoding gaussian mixture model for unsupervised anomaly detection." International conference on learning representations. 2018.

[3]: Liu, Fei Tony, Kai Ming Ting, and Zhi-Hua Zhou. "Isolation forest." 2008 eighth ieee international conference on data mining. IEEE, 2008.

[4]: Hariri, Sahand, Matias Carrasco Kind, and Robert J. Brunner. "Extended isolation forest." IEEE Transactions on Knowledge and Data Engineering 33.4 (2019): 1479-1489.

[5]: Liu, Fei Tony, Kai Ming Ting, and Zhi-Hua Zhou. "On detecting clustered anomalies using SCiForest." Machine Learning and Knowledge Discovery in Databases: European Conference, ECML PKDD 2010, Barcelona, Spain, September 20-24, 2010, Proceedings, Part II 21. Springer Berlin Heidelberg, 2010.

[6]: Choudhury, Jayanta, et al. "Hypersphere for Branching Node for the Family of Isolation Forest Algorithms." 2021 IEEE International Conference on Smart Computing (SMARTCOMP). IEEE, 2021.


