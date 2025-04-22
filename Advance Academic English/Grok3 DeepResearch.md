### Key Points

- Research suggests GAI poses challenges to academic integrity, especially in essay writing, with varying governance across regions.
- It seems likely that current policies lag behind GAI development, necessitating new governance models.
- The evidence leans toward using corpus linguistics and AI methods for analysis, with potential for AI-based detection systems.

---

### Background and Scope

Your research on "The Challenges and Governance Mechanisms of Academic Integrity in the Age of Artificial Intelligence" is timely, given GAI's rapid advancement and its impact on higher education, particularly essay writing. Given your 2-3 month timeline, focusing on a systematic literature review and corpus analysis of scholarly articles in English and Chinese will be feasible. This approach will help identify challenges and propose policy-focused governance mechanisms, potentially including AI-based detection, while acknowledging the complexity of regional differences and the need for comprehensive strategies.

### Data and Methods

For data, use Scopus for English and CNKI for Chinese to retrieve relevant articles, as student essays may not be publicly accessible within the timeframe. Employ quantitative linguistic methods like keyword analysis, n-grams, and sentiment analysis, leveraging Python for efficiency. Consider deep learning for enhanced analysis, such as topic modeling, to uncover trends. This comparative approach will highlight language-specific insights, enhancing your governance proposals.

### Governance and Detection

Your governance mechanism should focus on policies defining acceptable GAI use, citation practices, and educational programs. While developing an AI-based detection system from scratch is unrealistic in 2-3 months, you can review existing tools like GPTZero ([AI Detection](https://guides.library.ttu.edu/artificialintelligencetools/detection)) and propose their integration into a framework, addressing their limitations and biases.

---

### Detailed Research Plan and Insights

This section provides a comprehensive guide to optimize your thesis, deepen your understanding through literature, and enhance your research methods, particularly using Python for corpus analysis and proposing governance mechanisms. It includes all relevant details from your initial plan, refined for feasibility and effectiveness.

#### Introduction and Background

Your initial plan highlights GAI's rapid development and its challenges to academic integrity, especially in essay writing, with a lack of comprehensive governance and regional disparities. This is supported by recent studies, such as [The rapid rise of generative AI and its implications for academic integrity: Students’ perceptions and use of chatbots for assistance with ...](https://www.sciencedirect.com/science/article/pii/S2666920X24000766), which found over a third of Australian university students using chatbots for assessments without perceiving it as a breach, underscoring the need for clear policies.

Given your focus on higher education and analysis in English and Chinese, this research aligns with global trends, as seen in [Generative AI and the future of higher education: a threat to academic integrity or reformation? Evidence from multicultural perspectives | ...](https://educationaltechnologyjournal.springeropen.com/articles/10.1186/s41239-024-00453-6), which surveyed 1,217 participants across 76 countries, highlighting multicultural concerns.

#### Optimizing for Time Constraints

With only 2-3 months, your original plan to review previous research, analyze essays, and propose new methods is ambitious. To make it manageable, focus on a systematic literature review of scholarly articles rather than student essays, as accessing the latter is challenging. This shift is supported by [Reassessing academic integrity in the age of AI: A systematic literature review on AI and academic integrity](https://www.sciencedirect.com/science/article/pii/S2590291125000269), published in 2025, which provides a model for your approach.

#### Data Sources and Collection

Your initial data sources included "theses in the essay database" and "regulation files from high schools," but given your focus on higher education, clarify that you mean scholarly articles. Use Scopus for English and CNKI for Chinese, as these databases are accessible and contain relevant literature. For example, search terms like "generative AI," "academic integrity," and "governance" will yield results, as seen in [Academic Integrity in the Age of AI | EDUCAUSE Review](https://er.educause.edu/articles/sponsored/2023/11/academic-integrity-in-the-age-of-ai), which discusses policy needs.

Regulation files can be supplementary, analyzed qualitatively to understand institutional responses, but prioritize literature for corpus analysis.

#### Research Methods: Corpus Linguistics and Python Implementation

Your plan for quantitative linguistic analysis is sound, using methods like keyword analysis, n-grams, and sentiment analysis. Given your interest in deep learning, consider topic modeling for richer insights. Here's how to implement these using Python:

- **Keyword Extraction and Frequency Analysis:** Use libraries like `rake-nlp` or NLTK for keyword extraction. For example:
  ```python
  from rake_nlp import Rake
  text = "Your text here"
  rake = Rake()
  keywords = rake.apply(text)
  print(keywords)
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
  text = "Your text here"
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

#### Comparative Analysis: English vs. Chinese

Your focus on English and Chinese is insightful, given their global usage. Analyze trends in governance discussions, such as policy focus in English articles versus cultural attitudes in Chinese, as seen in [A comprehensive AI policy education framework for university teaching and learning | International Journal of Educational Technology in Higher ...](https://educationaltechnologyjournal.springeropen.com/articles/10.1186/s41239-023-00408-3), which studied Hong Kong universities.

Use bilingual corpus tools to compare keyword frequencies and sentiment, highlighting regional differences in academic integrity perceptions.

#### Governance Mechanisms and AI-Based Detection

Your goal to propose a new method or model is ambitious, but given time, focus on a policy-focused framework. Review existing university policies, such as [Examples of possible academic integrity policies that address student use of generative AI tools - Eberly Center - Carnegie Mellon University](https://www.cmu.edu/teaching/technology/aitools/academicintegrity/index.html), which offers adaptable guidelines.

Propose a model including:
- Definitions of GAI use (e.g., editing vs. generating full essays).
- Citation practices for AI-generated content.
- Educational programs for students and faculty.
- Integration of detection tools, reviewing options like GPTZero ([AI Detection](https://guides.library.ttu.edu/artificialintelligencetools/detection)) and their limitations, as discussed in [I tested 10 AI content detectors - and these 3 correctly identified AI text every time | ZDNET](https://www.zdnet.com/article/i-tested-10-ai-content-detectors-and-these-3-correctly-identified-ai-text-every-time/), noting inconsistencies.

Developing a detection system is infeasible in 2-3 months, but you can propose a framework, leveraging existing tools and addressing biases, especially for non-native speakers.

#### Time Management and Feasibility

Allocate your time as follows:
- Week 1: Literature search and article retrieval.
- Weeks 2-3: Reading, note-taking, and qualitative analysis.
- Week 4: Corpus analysis using Python.
- Week 5: Draft governance mechanism and detection discussion.
- Weeks 6-7: Writing and revisions.

This ensures a balanced approach, focusing on depth rather than breadth.

#### Unexpected Insight: Regional Policy Disparities

An unexpected finding from the literature is the significant variation in GAI governance across regions, with Western institutions often emphasizing detection tools, while East Asian contexts, like China, may focus on cultural education, as seen in [Generative AI in higher education: A global perspective of institutional adoption policies and guidelines - ScienceDirect](https://www.sciencedirect.com/science/article/pii/S2666920X24001516). This comparative angle can enrich your analysis.

#### Table: Summary of Research Methods and Tools

| **Method**         | **Description**                   | **Python Library**           | **Example Use**                |
| ------------------ | --------------------------------- | ---------------------------- | ------------------------------ |
| Keyword Extraction | Identify frequent terms           | `rake-nltk`, `NLTK`, `jieba` | Extract key themes in articles |
| N-gram Analysis    | Analyze word pairs/triplets       | `NLTK`                       | Identify common phrases        |
| Sentiment Analysis | Assess text positivity/negativity | `TextBlob`                   | Gauge attitudes toward GAI     |
| Topic Modeling     | Discover underlying themes        | `Gensim (LDA)`               | Cluster articles by topic      |

This table organizes your analytical approach, ensuring clarity in implementation.

#### Conclusion

By focusing on a literature review and corpus analysis, you'll identify GAI's challenges and propose a governance mechanism, potentially influencing policy in higher education. This approach leverages your strengths in linguistic analysis and Python, while addressing the complexity of regional and linguistic differences.

---

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