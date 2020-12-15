# Metagenomics
## Machine Learning Meta-analysis of Large Metagenomic Datasets


### Microbiome

>The human gut contains trillions of microbial inhabitants, making it one of the most densely populated environments on the planet. The symbiosis between these organisms and the human host is extremely complex, and we are only beginning to understand the impact of the gut microbiota on human biology. Knowledge of the chemical reactions performed and compounds produced by gut microbes will provide new insights into their roles in influencing human health. By studying the gene content of the human gut microbiome and the enzymes encoded by these genes, we hope to better understand the chemical capabilities of this microbial community. However, the activities of the vast majority of enzymes found in microbiomes are unknown.<br>
Shotgun metagenomic sequencing is a relatively new sequencing approach that allows insight to be gained into community biodiversity and function.
The function of shotgun metagenomic sequencing is to sequence the genomes of untargeted cells in a community in order to elucidate community composition and function.
Research using the method, taps into several fields due to the broad existence of large microbial communities. For example, the study of soil microbiota has led to advances in understanding and treating plant pathogens.
In human gut microbiota, the use of shotgun metagenomics discovered how common antibiotic genes are in our gut bacteria. <br>

By [Sara Ryding](https://www.news-medical.net/life-sciences/Shotgun-Metagenomic-Sequencing.aspx).

### Dataset

The dataset used in this project was created by the team of Edoardo Pasolli, Duy Tin Truong, Faizan Malik, Levi Waldron, and Nicola Segata who published a [research article in July of 2016 ](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004977), and created [MetAML](https://github.com/segatalab/metaml#metaml---metagenomic-prediction-analysis-based-on-machine-learning)  - Metagenomic prediction Analysis based on Machine Learning.

The authors used 8 publicly available metagenomic datasets, and applied MetaPhlAn2 to generate species abundance features. Their goal was to classify diseases using obtained abundance features, and to determine best ML models for this task. Though their experiments they settled on RandomForest as the best classifier for most diseases, with SVM doing better for some diseases.

### New tasks
Can we get **better predictions**? Different models? Ensembling? <br>
Can we find **which sets of species define better predictions**, and therefore related to specific diseases?<br>

I treat the problem as binary classification. Using XGBClassifier I analyze how well different diseases could be predicted against control samples, and against joint data of controls and other disesases. Through my experiments I found that Cirrhosis is the easiest to predict with extremely high precision. I use AUC and F1 metrics, to be able to compare my results with the paper's results.<br>
I also try to discriminate Cirrhosis from other diseases using the same approach.

### Acknowledgements

*Citation*: Pasolli E, Truong DT, Malik F, Waldron L, Segata N <br>
(2016) Machine Learning Meta-analysis of Large Metagenomic Datasets: Tools and Biological Insights. <br>
PLoS Comput Biol 12(7): e1004977.<br>
doi:10.1371/journal.pcbi.1004977
