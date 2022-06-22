# Digital Transformation


### Course Paper Syllabys 

1) All data of articles are uploaded to the repository's path: ./data/*.csv
    - data in Scopus and PubMed participated in the analysis
2) All preprocessing data are placed to the repository's path: ./data_network/*
    - here you can find preliminary lda model data and prepared data for the network
3) The script LDA_modeling.ipynb shows all the stages of data protection and building a thematic model.
4) The Network_modelling.ipynb script includes a description of the following result:
    - preparation of data for building a network;
    - search for clusters
    - building a network of co-authorship and subsequent clustering of authors
    - visualization of a network of clusters of co-authorship
    - comparison of clusters of the network of co-authorship and topics of the thematic model
    - evaluating clusterization by another methods


### 1. Introduction  

This project is aimed at studying the topic of "Digital Transformation" in the scientific community . The current field of knowledge began to develop rapidly in the last 20 years, however, due to the variety of tools and published articles, at the moment this field of knowledge does not have a knowledge-intensive foundation for building methodologies and general concepts, which contributes to the development of many different trends and groups of opinions. In this regard, there is an increasing interest in studying these trends and their distribution in the network of the current community. During the project, it is planned to systematically approach the identification of key groups of opinions (communities) and topics, as well as delve into the study of the distribution of trends/ideas/themes among network members (for example, showing which scientists introduce new scientific concepts or connections of scientific concepts, which are then adopted many others, how certain trends/ideas spread on the timeline, etc.). The results of this project will contribute to a better understanding of the field of knowledge "Digital Transformation", in particular which communities should be monitored now, who sets trends and who supports them, as well as which main themes/trends/concepts are now put forward and disclosed, and which require further study

*Due to the inability to upload data in all areas, the studied area of knowledge was narrowed down to the consideration of the "Digital Transformation" communities in healthcare (within this course, it is planned to continue the work in the future).

### Goal
Показать как устроена область знаний по Цифровой трансформации в сфере здравохранении, какие есть сообщества и интересы.

To find out how is organized the area of knowledge of DT healthcare: what kind of communites and interests there are? 


### 2. Main part

#### 2.1. Literature Review

In the past several years studies have started to appear comparing the accuracies of various science mapping approaches. These studies focus attention on the advantages and disadvantages of existing approaches.

There are three main citation-base approaches:
1) Bibliographic coupling (Kessler, 1963)
2) Co-citation Analysis (Marshakova, 1973; Small, 1973)  
    - Document Co-citation Analysis (DCA) (Chen, 2004; Chen, 2006; Chen, Song, Yuan, & Zhang, 2008)
    - Author Co-citation Analysis (ACA) (Chen, 1999; Leydesdorff, 2005; White & McCain, 1998; Zhao & Strotmann, 2008b)
3) Direct citation (cf., Shibata, Kajikawa, Takeda, & Matsushima, 2008)

These cited approaches have some disadvantages for identify clusters. 
In a longitudinal dataset where links are restricted to those within the set, bibliographic coupling is able to cluster very recent papers but clusters fewer of the very old papers, while co-citation clustering does the opposite – it clusters the older papers, but cannot cluster the most recent papers that have not yet been cited. Direct citation clusters documents more evenly across the time window, and tends to cluster a larger number of documents than either bibliographic coupling or co-citation processes. 

To improve results, we can:
-	Mixed cited approaches - Small (1997)
-	Use external references
 


#### 2.2. Anticipated Methods
- The co-authorship network was implemented by 3565 authors who wrote more than 2 papers on this topic. For each author, an identifier was assigned, which was assigned to the articles. The final network consists of 40,913 edges and 3565 points.
- For building a thematic model was used processed data of brief descriptions of all articles
- To identify communities in co-authorship network was used Kmeans algorithm and subsequent optimization of the "Elbow method".
- To evaluate clusterization by other algoritms 

#### 2.3. Anticipated Results

The analysis of the current network made it possible to identify key authors who have a tangible impact on the chosen field of knowledge.
The network model of co-authorship, according to its connections, shows the interaction between authors, so that the selected communities can be similar in their interests within their groups. Based on this assumption, it is possible to put forward a hypothesis about the presence of a coincidence of the identified thematic groups and community groups within the network of co-authorship.
The presence of communities of authors and selected thematic groups made it possible to analyze the interests of researchers in a particular community.

### 3.Conclusion
As part of this work, an analysis was made of a network of co-authors dedicated to digital transformation in the healthcare sector.
First, to identify subject areas of knowledge, a pool of studies was formed from the bases of scientific periodicals National Library of Medicine (PubMed) and Scopus for the period 2000-2022. The search was carried out both by keywords, article titles, and by the presence of a mention in the short description of the article. The total number of collected articles was 20889 pieces. Next, a co-authorship network was built. As a result of the analysis, a network of 40,913 edges, 3565 points was formed. Based on this network, it was possible to identify the authors with the largest number of connections, as well as the authors with the highest measure of mediation centrality. The next step in the study was to compare thematic groups on the one hand and clusters of authors on the other (which were identified using the Kmeans algorithm). After the comparison, a visualization of the network was presented and conclusions were drawn. These conclusions were verified using other network clustering algorithms, which ultimately proved once again the predominance of one large group of authors among the entire community.

Limitations:
  - dataset (need to expand the initial data and include more publications)
  - one-way network of co-authorship (needs to be supplemented with co-citation networks)


### 4.References 
- https://github.com/bavla/BibNets Vlado Batagelj
- Boyack, Kevin & Klavans, Richard. (2010). Co-Citation Analysis, Bibliographic Coupling, and Direct Citation: Which Citation Approach Represents the Research Front Most Accurately?. Journal of the American Society for Information Science and Technology. 61. 2389-2404. 10.1002/asi.21419. 
- Chaomei Chen, Fidelia Ibekwe-Sanjuan, Jianhua Hou. The Structure and Dynamics of Co Citation Clusters: A Multiple Perspective Co-Citation Analysis.. Journal of the American Society for Informa- tion Science and Technology, Association for Information Science and Technology (ASIS&T), 2010, 61 (7), pp.1386-1409. 10.1002/asi.21309 . hal-00638091
- Inf2vec: Latent Representation Model for Social Influence Embedding https://ieeexplore.ieee.org/document/8509310 
- Vladimir Batagelj: On Fractional Approach to Analysis of Linked Networks.
- Vladimir Batagelj, Daria Maltseva: Temporal Bibliographic Networks.
- Boyack KW, Newman D, Duhon RJ, Klavans R, Patek M, et al. (2011) Clustering More than Two Million Biomedical Publications: Comparing the Accuracies of Nine Text-Based Similarity Approaches. PLoS ONE 6(3): e18029. doi:10.1371/journal.pone.0018029
- LDAvis: A method for visualizing and interpreting topics
- https://www.jmlr.org/papers/volume3/blei03a/blei03a.pdf 
