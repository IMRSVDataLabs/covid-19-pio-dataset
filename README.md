
<h1>Extraction of Population, Intervention, and Outcome sentences from 33,000 Coronavirus (COVID-19) Full-Text Research Articles</h1>

IMRSV Data Labs, an artificial intelligence company from Canada, has applied an internally developed Natural Language Processing (NLP) algorithm on a large dataset of full-text COVID-19 research in order to extract Population, Intervention, and Outcome sentences from the full-text articles and is releasing this data publicly. Our aim is for COVID-19 researchers to use this as a text-mining tool to provide insights on research questions.

<h2>About the data</h2>

The dataset of full-text articles on which our algorithm was applied was released as part of the COVID-19 Open Research Dataset Challenge (CORD-19). For more information about the dataset, see [2].

<h2>Methodology and Definitions</h2>

Clinical questions are often formed using the PIO framework, where clinical issues are broken down
into four components: Population/Problem (P), Intervention (I), and Outcome (O). It was found that using the PIO framework can significantly improve literature screening efficacy. Therefore, efficient extraction of PIO elements is a key feature of many evidence based medicine applications. 

We have trained and applied a model that singles out and identifies sentences from ~33,000 full-text articles found [1] in an effort to help researchers narrow down articles of interest. The machine learning classification model used a BERT representation by adding a dense layer corresponding to the multi-label classifier with three output neurons corresponding to PIO labels.  (Source [2].)

<h2>How Researchers Can Use This Resource</h2>

Such a dataset could help researchers sort through the vast amount of research by providing a starting point with regards to PIO identification, even if approximate by such an algorithm. It must be noted that the sentences that are identified as P, I, and O in this dataset have not been reviewed by humans, and were identified by a machine learning model as potentially having the same grammatical structure and may contain similar words as identified by a machine learning model. For example, a sentence may talk about patients but it does not necessarily mean that this is the population that was studied in the full-text article. However, it may still be useful to identify articles that contain those sentences and to seek the full context that can be downloaded by looking at the complete articles at [1].

<h2>Data dictionary</h2>

Each row of data reports a sentence from either the body or the abstract of an article that has been successfully classified as a sentence that may contain relevant information pertaining to the Population, Intervention, or Outcome.

| **Column Name**      | Description                 |
|--------------|----------------------------------------------------------------------------------------|
| **sha**      | The unique sha corresponding to the article where the full text article can be obtained by downloading the dataset at [1].                    |
| **PMID**     | The pubmed ID of the article, if available.                                            |
| **section**  | The location of the sentence within the article. |
| **sentence** | The sentence, as found in the article.                                                 |
| **P**        | The confidence of the sentence discussing population.                                  |
| **I**        | The confidence of the sentence discussing intervention.                                |
| **O**        | The confidence of the sentence discussing outcome.                                     |

<h2>License and Attribution</h2>

We are making this data publicly available for broad, noncommercial public use including by medical and public health researchers.

If you use this data, we would appreciate it if you would attribute it to “IMRSV Data Labs”  and link to our webpage at https://www.imrsv.ai.

See our LICENSE for the full terms of use for this data.

This license is co-extensive with the Creative Commons Attribution-NonCommercial 4.0 International license, and licensees should refer to that license (CC BY-NC) if they have questions about the scope of the license.

<h2>Contact Us</h2>

If you have questions about the data or licensing conditions, please contact us at:

x@imrsv.ai.

<h2>Contributors</h2>

Data has been compiled by Aleksandr Gontcharov using internally trained models with help from colleague Hichem Mezaoui at
IMRSV Data Labs, Ottawa, Canada.
www.imrsv.ai

<h2>References</h2>

[1] https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge

[2] Hichem Mezaoui, Aleksandr Gontcharov, Isuru Gunasekara, https://arxiv.org/abs/1906.11085 Enhancing PIO Element Detection in Medical Text Using Contextualized Embedding,  June 2019





