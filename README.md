# SpikesLS

High-density neural recordings from neuropixels probes require accurate spike detection to interpret neuronal activity. While standard tools like Kilosort rely on a template matching approach, they can be limited in handling variability and overlapping spikes. In this study, we explore an alternative strategy using sparse plus low-rank decomposition, formulated as a Principal Component Pursuit problem. We compare three solvers, PG, ADMM and GoDec, on their ability to extract spikes from submatrices of the channel×time data. Due to Kilosort’s output constraints, evaluation focuses on spike timing rather than channel comparison. Both supervised and unsupervised metrics reveal that PG and ADMM offer stronger performance, while GoDec shows promise for larger datasets. Although recall can be satisfactory, lower precision suggests some false detections or missed spikes by Kilosort. Future work could integrate sparse decomposition with template-based approaches for more flexible and robust spike detection

# Repository structure
The repository contains all the Python code needed to process the data used to create and validate SafeStart. A brief description of each notebook file is given below. \
**SpikesLS_main.ipynb** : Main notebook containing the code for the three solvers, hyperparameters investigation and impact of matrix size.\
**plot_res.ipynb** : Produces all the results from the .csv files provided by the main notebook\
