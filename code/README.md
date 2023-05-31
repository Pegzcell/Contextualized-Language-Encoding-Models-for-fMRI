# Incorporating Context into Language Encoding Models for fMRI
**Project by Team - Synaptic**
- Pratham Gupta
- Amal Sunny
- Aayush Bhandari

Language encoding models help explain language processing in the human brain by learning functions that predict brain responses from the language stimuli that elicited them. Current word embedding-based approaches treat each stimulus word independently and thus ignore the influence of context on language understanding. This work instead builds encoding models using rich contextual representations derived from an LSTM language model ultimately aiming to show a significant improvement in encoding performance relative to state-of-the-art embeddings in nearly every brain area. 

## Acknowledgements
------------
This fMRI data used in our project was collected by Alex Huth and Wendy de Heer at the University of California, Berkeley. All work was supervised by professors Jack Gallant and Frederic Theunissen of the UC Berkeley Psychology Department. Visualization is done using [pycortex](http://pycortex.org).

## The experiment
------------
In this experiment a subject underwent fMRI scanning while they listened to roughly 2 hours of natural narrative speech stimuli. These stimuli were 10-15 minute complete stories drawn from *The Moth Radio Hour*, a radio program where storytellers tell true, autobiographical stories in front of a live audience.

## Installation
------------
1. The data and result pickle files have been ommitted in this directory due to memory constraints. reach out to any of the team members if you want to run the code.
2. (If not using Anaconda) install dependencies:
`sudo apt-get update`
`sudo apt-get install -y ipython ipython-notebook python-numpy python-scipy python-matplotlib cython python-pip python-pip python-dev python-h5py python-nibabel python-lxml python-shapely python-html5lib mayavi2 python-tables git`
1. Fetch and install pycortex:
`git clone https://github.com/gallantlab/pycortex.git`
`cd pycortex; python setup.py install`
1. Start a Jupyter notebook server in this directory:
`jupyter notebook`

## File Descriptions
------------
- ***pipeline.ipynb*** - stores the main pipeline of the research including analysis on the english1000 model (baseline embeddings) and on Layer12 analogous to it (barring cortical visualization).
- ***analysis.ipynb*** - stores the code to represent contextual encoding model performance with different context lengths and layers vs.state-of-the-art embedding.
- ***analysis_swapped.ipynb*** - stores the code to represent contextual encoding model performance after swapping context between different occurrences of each word and re-fit the encoding models with different context lengths and layers vs.state-of-the-art embedding.
- ***getcorrs.ipynb*** - stores the code to get the correlation values from the fmri data regression models that are used to visualize the activations across the cortices.
- ***analysis_cortex.ipynb*** - stores the code to visualize the importance of contextual information for representations
in each area of the cortex.
