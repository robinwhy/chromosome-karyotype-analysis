# chromosome-karyotype-analysis
The karyotype analysis consists of three main parts-chromosome segmentation, chromosome classification and anomaly annotation, this project provides a foundation for the whole process.
## chromosome segmentation
**rawseg.ipynb** segments single chromosomes from a raw cell image based on thresholding and other computer vision skills, remaining are overlapping or touching chromosomes which can be handled by Unet.
## chromosome classification
**karyotype_segment.ipynb** segments single chromosomes from manually labeled karyotype images, providing the training data for classification purpose since classification requires single images.
class_karyotype.ipynb classifies each single chromosome into its class.
## anomaly annotation
There are two kinds of anomalies in chromosomes. The first is numerical problem, namely the addition or loss of a single or more chromosomes. **numerical.ipynb** solves this part by simply counting the number of connected components in karyotype images.
The second is structural problem, containing translocation, duplication, deletion etc. There is few researcher focusing on this field and there is no public data about the problem. **class_translocation.ipynb** tackles the translocation problem based on our own dataset, but for other cases, not enough data is available, which warrants future study.
