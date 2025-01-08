# Social Group Mentions 
This project explores the identification of "Social Group Mentions" in social media texts. 

The repository contains:
- [Annotation guidelines](Annotation%20Guidelines%20for%20Identification%20of%20Social%20Group%20Mentions.pdf) for identifying social group mentions
- A non-aggregated dataset, Reddit-Social Group Mentions (Reddit-SGM)
- A Taxonomy of Human Label Variation in Identification of Social Group Mentions

## Project Summary
Social Groups (In the literature, closely related terms include [Identity Groups](https://aclanthology.org/2022.naacl-main.410.pdf) and [Group Reference](https://aclanthology.org/2024.lrec-main.701.pdf)) are a prime example of complex and ambiguous social concepts that have only recently garnered attention in natural language processing (NLP) research, particularly within the emerging field of perspectivism. Following this line of research, we propose that disagreements between annotators in the identification of social group mentions  provide important insights into what constitutes a social group. By analyzing diverging annotation judgments, we develop **a taxonomy of human label variation** that distinguishes between ambiguities in identifying social group mentions and genuine annotation errors. Our findings reveal that linguistic and interpretative ambiguities represent a majority of variation when it comes to subjective and ambiguous concepts, underscoring the complex and multifaceted nature of social group mentions. To explore this, we present **Reddit- Social Group Mentions (Reddit-SGM)**, a novel, non-aggregated dataset for studying social group mentions in texts.

## Source of Reddit-SGM Dataset
Using data from the [Reddit Politosphere dataset](https://zenodo.org/records/5851729), we created Reddit-Social Group Mentions (Reddit- SGM). Due to the labor-intensive nature of human annotation and budget constraints, we randomly selected approximately 2K comments from the five most popular subreddits in the Reddit Politosphere dataset, based on comment counts over the 12-year span (2008–2019). The Reddit-SGM dataset encompasses the following five subreddits: **r/politics**, **r/ukpolitics**, **r/Libertarian**, **r/Economics**, and **r/worldpolitics**.
### Corpus statistics for Reddit-SGM

|# | r/politics | r/Economics | r/worldpolitics | r/ukpolitics | r/Libertarian
|     :---:    |     :---:      |     :---:      |     :---:    |     :---:      |     :---:      |
| Comments   |  408  | 408  |  408  | 408  | 408  | 
| Sentences     | 1,336 | 1,542 | 1, 314 | 1,201 | 1,486|
| Words     | 18,664  |  23,368 | 20,185 | 20,808 | 23,255
| Sentences by Comments| 3.27| 3.77| 3.21| 2.94| 3.63|
|Words by Comments|45.63 | 57.13 | 49.35| 50.88| 56.86 |

## Data Annotation Process
We started with an experiment using 600 randomly selected comments from r/politics, to ensure accuracy in the task of identifying spans of social group mentions and developing the annotation guidelines. This data was utilized in a [preliminary study](https://dl.acm.org/doi/10.1145/3630744.3658412) to assess the potential of automatic identification of social group mentions and not subsequently included in the Reddit-SGM corpus. The [annotation guidelines](Annotation%20Guidelines%20for%20Identification%20of%20Social%20Group%20Mentions.pdf)  were developed iteratively, evolving from an initial draft used in the prestudy that simply defined social group mentions and provided examples, to a refined version incorporating examples of nuanced cases to achieve the desired precision.
### Who are the annotators?
The annotations for Reddit-SGM were completed by three undergraduate students: two from social science and one from computer science. We trained them by providing annotation guidelines and conducting discussions during training meetings. During these meetings we had them annotate challenging test examples to ensure they understood the task. This training was crucial to maintain consistency in their work.

## Method for Analysis of Label Variation
Label variation in our context refers to discrepancies between annotations of social group mentions provided by different human annotators [9]. For instance, consider the text snippet: **I think Wells Fargo has almost 2 trillion dollars in assets**. One annotator might label **Wells Fargo** as a social group mention and argue that it refers to the corporation as a group of people. However, the others may perceive the corporation as simply an organizational structure and do not annotate it, resulting in label variation. 

The below flowchart shows how annotators independently label comments containing social group mentions (highlighted in bold). Mentions with disagreements between annotators (2,813) are flagged as containing label variation. Domain experts review approximately 20% (520) of these flagged mentions to develop a taxonomy of label variation. Subsequently, the material was reviewed again by domain experts, around half (1,568) of these flagged mentions are annotated with reasons for label variation, and these annotations are released along with the Reddit-SGM dataset.

![screen](https://github.com/FaraneJalaliFarahani/Social-Group-Mentions/blob/main/Flowchart.png)
