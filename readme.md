<!-- PROJECT LOGO -->
<br />
<div align="center">
    <img src="images/Traveloka_idgaNgeFw0_1.png" alt="Logo" width="300" height="70">

  <h2 align="center">Traveloka Sentiment Analysis</h2>

  <p align="center">
    IDCamp Intermediate First Project
  </p>
</div>

<!-- ABOUT THE PROJECT -->
#### About The Project

This project aims to perform sentiment analysis on Traveloka Play Store Reviews from the Google Play Store. The analysis classifies user reviews into three sentiment polarities: **Positive, Neutral, and Negative**.

#### Built With

Framework/libraries used.

* [![TensorFlow][TensorFlow.js]][TensorFlow-url]
* [![Pandas][Pandas.py]][Pandas-url]
* [![Jupyter][Jupyter.org]][Jupyter-url]
* [![Transformers][Transformers.hw]][Transformers-url]
* [![Scikit-Learn][Scikit-Learn.org]][Scikit-Learn-url]


<!-- GETTING STARTED -->
#### Getting Started

The dataset used consists of user reviews for the Gojek application, collected using scraping techniques from the Google Play Store.

- **Source:** Traveloka Google Play Store Reviews
- **Dataset row:** 62,190 rows
- **Data Split:** 70% Training, 30% Testing
- **Preprocessing:** Cleaning, Case Folding, Normalization (Slang words), Stopword Removal, Stemming (untuk Model Non-BERT).

## Experiment Schemes & Methodology
To achieve the best results, this project conducted experiments using 3 different model schemes:

#### Model 1: Traditional Machine Learning (Baseline)
- **Model:** Support Vector Machine (SVM)
- **Feature Extraction:** TF-IDF (Term Frequency-Inverse Document Frequency)
- **Purpose:** To serve as a performance baseline for comparison against Deep Learning models.

#### Model 2: Deep Learning (RNN Architecture)
- **Model:** Bidirectional LSTM (Bi-LSTM)
- **Feature Extraction Model:** Word2Vec (Custom Trained Embeddings)
- **Arch:** Embedding Layer -> Bi-LSTM -> Dropout -> Dense Layer (Softmax).
- **Purpose:** To capture word sequence context (sequential data) that cannot be captured by TF-IDF.

#### Model 3: Transformers
- **Model:** IndoBERT (BERT-base model trained on Indonesian corpus)
- **Approach:** Fine-tuning pre-trained model `sarahlintang/IndoBERT`.
- **Purpose:** To leverage a language model that already possesses a deep understanding of the Indonesian language context.

## Results & Evaluation

 | Algorithm | Training Accuracy | Testing Accuracy | Training Loss | Testing Loss |
| :--- | :--- | :--- | :--- | :--- |
| SVM + TF-IDF | 96 | 94 | - | - |
| Bi-LSTM + Word2Vec | 98 | 95 | 0.1 | 0.2 |
| IndoBERT | 97 | 95 | 0.07 | 0.1 |

<!-- LICENSE -->
## License

Feel free to modify!

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Resources i find helpful and would like to give credit to.

* [Huggingface](https://huggingface.co/)
* [Tensorflow](https://www.tensorflow.org/)
* [Dicoding](https://www.dicoding.com/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[TensorFlow.js]: https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white
[TensorFlow-url]: https://www.tensorflow.org/

[Pandas.py]: https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white
[Pandas-url]: https://pandas.pydata.org/

[Jupyter.org]: https://img.shields.io/badge/Jupyter-%23F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white
[Jupyter-url]: https://jupyter.org/

[Transformers.hw]: https://img.shields.io/badge/%F0%9F%A4%97%20Transformers-blue?style=for-the-badge
[Transformers-url]: https://huggingface.co/docs/transformers/index

[Scikit-Learn.org]: https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white
[Scikit-Learn-url]: https://scikit-learn.org/