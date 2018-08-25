Learning Latent Factors for Community Identification and Summarization (LFCIS)

This repository contains the materials related to the manuscript "Learning Latent Factors for Community Identification and Summarization," including the drafted version of the final paper, and the executable of the algorithm.

As this paper is open access, you may also find the published version of it via https://ieeexplore.ieee.org/document/8374421/. 

You are welcome to cite our paper via: T. He, L. Hu, K. C. C. Chan, and P. Hu, "Learning Latent Factors for Community Identification and Summarization," IEEE Access, vol. 6, pp. 30137-30148, 2018.


How to use LFCIS 

To use LFCIS (LFCIS.exe) to detect clusters in an attributed graph, please firstly prepare four files, which are named as "Config.txt," "edgelist," "vertex2aid," and "statistics" and put them into the directory where LFCIS.exe is. The detailed information for these files is the following:

edgelist: This file contains the connections in the attributed graph. There are two columns in this file which are the ids of source and target nodes. It should be noted that the starting node id must be 0.

vertex2aid: This file contains attributes that each vertex in the graph is associated with. There are two columns. The first column contains the vertex ids and the second column contains the ids of attributes that are labeled with each vertex. It should be noted that the starting ids for both node and attribute must be 0.

Config.txt: This file contains the parameters used by LFCIS. There are 6 reals in this file. They are the settings related to the number of clusters, alpha (parameter controlling the sparseness of A), sigma (parameter controlling the scale of the kernel function), the maximum number of optimizing iterations, the minimum change of C between two iterations, and the frequency that LFCIS computes the objective value within the optimization process. Here is an example: 4 0.5 1 300 1e-9 50 This means the initial settings of LFCIS are the following: 4 clusters, 0.5 alpha, 1 scale, 300 iterations of optimization, 1e-9 minimum change of C, and computing objective value every 50 iterations. These parameters can be modified accordingly, or one may follow recommendations in the paper of LFCIS.

statistics: This file contains the information of the attributed graph. Here is an example: 500 9000 50 It means this attributed graph contained 500 vertices, 9000 edges, and 50 attributes, respectively. To help users get familiar with the files used by LFCIS, we provide the corresponding files of a set of attributed graph data which are in the directory ".\example". One may check them for the details.

After completing all the preparations, one is able to run LFCIS to perform the task of clustering in attributed graph data by running a.bat file in which contains the following codes: "LFCIS.exe pause." The results of clustering in the attributed graph will be written into a file after LFCIS completes the optimization process. If LFCIS cannot be executed, please check readme.txt for the requirements of running environment, which is in the zip file.

Notice: This software is permitted to use only for research and non-commercial activities. If you have any question, please feel free to contact us via tiantian.he@outlook.com.

At last, thanks very much for using LFCIS.
