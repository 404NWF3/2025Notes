### Introduction and Background

Generative Artificial Intelligence has been developing rapidly, and it has posed challenges on academic integrity while students writing essays.  Research has found over a third of Australian university students using chatbots for assessments without perceiving it as a breach, underscoring the need for clear policies.[The rapid rise of generative AI and its implications for academic integrity: Students’ perceptions and use of chatbots for assistance with ...](https://www.sciencedirect.com/science/article/pii/S2666920X24000766). This research will focus on higher education and analysis in English and Chinese, retrieaving essays from researchers and regulations from governor in high education institutions. Considering there's only 2-3 months for us to conduct our research, to make it manageable, we only focus on scholarly articles rather than all student essays, and underscore the comparison between China and western countries emphatically via a computed linguistic methodology. What's more we will also try to launch a method to detect AI usage if possible.

### Data Sources and Collection

As for the data source, we will use Scopus for English and CNKI for Chinese, as these databases are accessible and contain relevant literature. For example, search terms like "generative AI," "academic integrity," and "governance" will yield results, which discusses policy needs. Regulation files can be supplementary, analyzed qualitatively to understand institutional responses, but prioritize literature for corpus analysis.

### Research Methods: Corpus Linguistics and Python Implementation

Your plan for quantitative linguistic analysis is sound, using methods like keyword analysis, n-grams, and sentiment analysis. Given your interest in deep learning, consider topic modeling for richer insights. Here's how to implement these using Python:

- **Keyword Extraction and Frequency Analysis:** Use libraries like `rake-nlp` or NLTK for keyword extraction. For example:
```python
from rake_nltk import Rake
text = ""
rake = Rake()
rake.extract_keywords_from_text(text)
keywords = rake.get_ranked_phrases()
print(keywords)
keywords_with_scores = rake.get_ranked_phrases_with_scores()
print(keywords_with_scores)
```
  
  For frequency, use NLTK:
```python
from collections import Counter
from nltk import word_tokenize

text = "Your text here"
words = word_tokenize(text)
word_freq = Counter(words)
print(word_freq.most_common(5))
```

- **N-grams and Sentiment Analysis:** Use NLTK for n-grams and TextBlob for sentiment:
```python
from textblob import TextBlob

text = "Shanghai is a great city"
blob = TextBlob(text)
print(blob.sentiment)
```

- **Topic Modeling with Deep Learning:** Use Gensim for Latent Dirichlet Allocation (LDA):
  ```python
  from gensim import corpora, models
  texts = [["human", "interface", "computer"], ["survey", "user", "computer", "system", "human"], ...]
  dictionary = corpora.Dictionary(texts)
  corpus = [dictionary.doc2bow(text) for text in texts]
  lda_model = models.LdaModel(corpus, num_topics=10, id2word=dictionary)
  topics = lda_model.print_topics(num_words=4)
  for topic in topics:
      print(topic)
  ```

These methods will help analyze articles in both languages, enabling comparison. For Chinese, ensure text preprocessing accounts for character-based analysis, using libraries like `jieba` for segmentation.


### Time Management and Feasibility

Allocate research time as follows:
- Week 1: Literature search and article retrieval.
- Weeks 2-3: Reading, note-taking, and qualitative analysis.
- Week 4: Corpus analysis using Python.
- Week 5: Draft governance mechanism and detection discussion.
- Weeks 6-7: Writing and revisions.


### Summary of Research Methods and Tools

| **Method**         | **Description**                   | **Python Library**           | **Example Use**                |
| ------------------ | --------------------------------- | ---------------------------- | ------------------------------ |
| Keyword Extraction | Identify frequent terms           | `rake-nltk`, `NLTK`, `jieba` | Extract key themes in articles |
| N-gram Analysis    | Analyze word pairs/triplets       | `NLTK`                       | Identify common phrases        |
| Sentiment Analysis | Assess text positivity/negativity | `TextBlob`                   | Gauge attitudes toward GAI     |
| Topic Modeling     | Discover underlying themes        | `Gensim (LDA)`               | Cluster articles by topic      |

### Key Citations

- [The rapid rise of generative AI and its implications for academic integrity: Students’ perceptions and use of chatbots for assistance with ...](https://www.sciencedirect.com/science/article/pii/S2666920X24000766)
- [Academic Integrity in the Age of AI | EDUCAUSE Review](https://er.educause.edu/articles/sponsored/2023/11/academic-integrity-in-the-age-of-ai)
- [Promoting Academic Integrity in the Age of Generative AI - John Spencer](https://spencereducation.com/ai-academic-integrity/)
- [Generative AI and the future of higher education: a threat to academic integrity or reformation? Evidence from multicultural perspectives | ...](https://educationaltechnologyjournal.springeropen.com/articles/10.1186/s41239-024-00453-6)
- [Reassessing academic integrity in the age of AI: A systematic literature review on AI and academic integrity](https://www.sciencedirect.com/science/article/pii/S2590291125000269)
- [Examples of possible academic integrity policies that address student use of generative AI tools - Eberly Center - Carnegie Mellon University](https://www.cmu.edu/teaching/technology/aitools/academicintegrity/index.html)
- [AI Detection - Artificial Intelligence Tools for Detection, Research and Writing - Guides at Texas Tech University](https://guides.library.ttu.edu/artificialintelligencetools/detection)
- [The best AI content detectors | Zapier](https://zapier.com/blog/ai-content-detector/)
- [11 Most Reliable AI Content Detectors: Your Guide To Spotting Synthetic Media](https://www.forbes.com/sites/bernardmarr/2024/11/21/11-most-reliable-ai-content-detectors-your-guide-to-spotting-synthetic-media/)
- [I tested 10 AI content detectors - and these 3 correctly identified AI text every time | ZDNET](https://www.zdnet.com/article/i-tested-10-ai-content-detectors-and-these-3-correctly-identified-ai-text-every-time/)