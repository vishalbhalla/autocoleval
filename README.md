# Evaluation of automatic collocation extraction methods for language learning

This repository contains the code for the paper on [Evaluation of automatic collocation extraction methods for language learning](https://www.aclweb.org/anthology/W19-4428) accepted at the [14<sup>th</sup> Workshop on Innovative Use of NLP for Building Educational Applications (BEA)](https://sig-edu.org/bea/current) at [The 57<sup>th</sup> Annual Meeting of Association for Computational Linguistics (ACL) 2019](http://www.acl2019.org/EN/index.xhtml).
Additionally, the [poster](https://www.researchgate.net/publication/335368166_Collocations_Poster_BEA_ACL_2019pdf) presented at the workshop.

## Installation
* Python 3.6+ (Install using [Anaconda](https://www.anaconda.com/distribution/) - Recommended and tested!)
* [Spacy](https://spacy.io/usage/)


## Data
Download the [Data and Evaluation files](https://drive.google.com/open?id=17eydi0KkviG2VxB12l_oNt5LAhuQ6FR0) for all the three test sets - Sketch Engine, FLAX and Elia.

**Note:** Elia is not available online yet, however, one can access the [code and data used to generate Elia's database of collocations](https://drive.google.com/open?id=1FGFy_yp797saphx8-wzcLkMxQbkCVZlp)


## Collocation Extraction

Extract collocates for each of the 3 test sets of Sketch Engine, FLAX and Elia.

1. For Sketch Engine (SE) and FLAX (FL), the collocations are web scraped as below, 
    - Open the Ipython notebook (**SketchEngine_WebScraping.ipynb** for Sketch Engine (SE) and **FLAX_WebScraping.ipynb** for FLAX (FL))
    - Change the path to point to the Reference Set
    - Change the location to store the Collocations data .csv files for Evaluation.
    - Run all cells in the notebook.

1. For Elia (EL), 
    - Open the Ipython notebook **CollocationsExtraction_Elia.ipynb**
    - Change the path to the .csv files for the Reference Set and Collocates Database from Elia.
    - Change the location to store the filtered Collocates .csv files scraped from Elia for Evaluation.
    - Run all cells in the notebook.

## Evaluation:

1. For Evaluation of all 3 test sets (Sketch Engine, FLAX and Elia), 
    - Open the Ipython notebook **Evaluation_Collocations.ipynb**
    - Change the path to the Reference Set, Collocation data .csv files and where the Evaluation files will be generated for each test set in its corresponding cell.
    - Run all cells in the notebook.

1. Open the generated evaluation files to compute the Precision and Recall metrics (per collocation type and for each of the test set).


## Results Plot:
1. For Plotting of Results many graph variants were used and the final one was selected. To run all of these,
    - Open the Ipython notebook **Results_Plot.ipynb**
    - Change path to the folder where the **Elia_CollocationMeasures_Comparison.csv** file (provided with the code) is located. By default this should be in the current directory and hence the variable 'plotDataFolder' need not be changed.
    - Run all cells in the notebook.
    - View the plots/graphs inline in the notebook or click on it to open it in a new tab to save it locally.


## Citation
If you use this paper in your research, we'd be appreciate if you cite the paper:

Evaluation of automatic collocation extraction methods for language learning, Bhalla, Vishal and Klimcikova, Klara, Proceedings of the Fourteenth Workshop on Innovative Use of NLP for Building Educational Applications (BEA), Association for Computational Linguistics (ACL). August 2019

or, in bibtex format:
```
@inproceedings{bhalla-klimcikova-2019-autocoleval,
    title = "Evaluation of automatic collocation extraction methods for language learning",
    author = "Bhalla, Vishal and Klimcikova, Klara",
    booktitle = "Proceedings of the Fourteenth Workshop on Innovative Use of NLP for Building Educational Applications (BEA) at The 57th Annual Meeting of The Association for Computational Linguistics (ACL)",
    month = August,
    year = "2019",
    address = "Florence, Italy",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/W19-4428",
    pages = "264--274",
    abstract = "A number of methods have been proposed to automatically extract collocations, i.e., conventionalized lexical combinations, from text corpora. However, the attempts to evaluate and compare them with a specific application in mind lag behind. This paper compares three end-to-end resources for collocation learning, all of which used the same corpus but different methods. Adopting a gold-standard evaluation method, the results show that the method of dependency parsing outperforms regex-over-pos in collocation identification. The lexical association measures (AMs) used for collocation ranking perform about the same overall but differently for individual collocation types. Further analysis has also revealed that there are considerable differences between other commonly used AMs.",
}
```
