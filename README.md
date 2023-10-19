# MiniBatch-K-means-Distributed-algorithms
This project has been developed to verify the advantage and disadvantage of a distributed MiniBatch K-means algorithm.
For this purpose CloudVeneto virtual machines were used. Indeed open source Apache Spark has provided the cluster computing framework required to test the algorithm performance. The algorithm has been developed in python.
In order to clarify the process, the developer undertakes to recommend a reading path for the different Jupyter Notebooks.

Project structure is the following:

1. Brief_Algorithm_Test.ipynb:
   a simple dataset has been produced to verify the work of the algorithm. The dataset is composed by 5 different blobs so the expectations are the clear clustering performed by the algorithm which has been satisfied. Here is performed the first version of the algorithm were only the processes were parallelized and the dataset instead remain in the master environment.
\
2. Processes_Parallelized.ipynb:
   as mentioned in the previous paragraph in this version of the algorithm only the processes were parallelized. Here has been used the fetch_rcv1.target dataset provided by ScikitLearn to test the algorithm.Testing means to perform algorithm with different partitions and different number of cores provided by the virtual machines. This notebook aims to show how performance data has been collected in this specific case.\
\
3. # Processes_DataFrame_Spark.ipynb:
   Here data has been parallelized using SparkDataFrame, the operating algorithm principle is the same but some changes were necessary to allows the algorithm to perform with SparkDataFrame object. Performing test consists in changing number of partition and number of cores, checking how the cost function and time execution change through this quantities. As previous mentioned his notebook aims to show how performance data has been collected in this specific case.\
   
4. # Processes_rdd_Spark.ipynb:
   Here RDD has been performed, less structured than SparkDataFrame but still parallelized in the Spark cluster. Performing test consists in changing number of partition and number of cores, checking how the cost function and time execution change through this quantities. As previous mentioned his notebook aims to show how performance data has been collected in this specific case.\
\
5. # BENCHMARK.ipynb :
   Here has been performed data analysis from data collected in the previous experiments. The main steps are showing time execution varying through number of partition and number of cores in the three configurations showed before, in a first moment thorough an heat-map and through a scatterplot, in the end has been showed how the mean squared error between points and cluster centers vary in relation to iterations.\
\


   
