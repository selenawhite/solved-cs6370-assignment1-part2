Download Link: https://assignmentchef.com/product/solved-cs6370-assignment1-part2
<br>
The goal of the assignment is to build a search engine from scratch, which is an example of an information retrieval system. In the class, we have seen the various modules that serve as the building blocks of a search engine. The first part of the assignment involved building a basic text processing module that implements sentence segmentation, tokenization, stemming/lemmatization and stopword removal. This module involves implementing an Information Retrieval system using the Vector Space Model. The same dataset as in Part 1 (Cranfield dataset) will be used for this purpose.

<ol>

 <li>Now that the Cranfield documents are pre-processed, our search engine needs a data structure to facilitate the ’matching’ process of a query to its relevant documents. Let’s work out a simple example. Consider the following three sentences:</li>

</ol>

S1 Herbivores are typically plant eaters and not meat eaters S2 Carnivores are typically meat eaters and not plant eaters

S3 Deers eat grass and leaves

Assuming <em>{are, and, not} </em>as stop words, arrive at an inverted index representation for the above documents (treat each sentence as a separate document).

<ol start="2">

 <li>Next, we must proceed on to finding a representation for the text documents. In the class, we saw about the TF-IDF measure. What would be the TF-IDF vector representations for the documents in the above table? State the formula used.</li>

 <li>Suppose the query is “plant eaters”, which documents would be retrieved based on the inverted index constructed before?</li>

 <li>Find the cosine similarity between the query and each of the retrieved documents. Rank them in descending order.</li>

 <li>Is the ranking given above the best?</li>

 <li><strong>Now, you are set to build a real-world retrieval system. Implement an Information Retrieval System for the Cranfield Dataset using the Vector Space Model</strong>.</li>

 <li>(a) What is the IDF of a term that occurs in every document?</li>

</ol>

(b) Is the IDF of a term always finite? If not, how can the formula for IDF be modified to make it finite?

<ol start="8">

 <li>Can you think of any other similarity/distance measure that can be used to compare vectors other than cosine similarity. Justify why it is a better or worse choice than cosine similarity for IR.</li>

 <li>Why is accuracy not used as a metric to evaluate information retrieval systems?</li>

 <li>For what values of <em>α </em>does the <em>F<sub>α</sub></em>-measure give more weightage to recall than to precision?</li>

 <li>What is a shortcoming of Precision @ K metric that is addressed by Average Precision @ k?</li>

 <li>What is Mean Average Precision (MAP) @ k? How is it different from Average Precision (AP) @ k ?</li>

 <li>For Cranfield dataset, which of the following two evaluation measures is more appropriate and why? (a) AP (b) nDCG</li>

 <li><strong>Implement the following evaluation metrics for the IR system</strong>:

  <ul>

   <li>Precision @ k</li>

   <li>Recall @ k</li>

   <li>F-Score @ k</li>

   <li>Average Precision @ k</li>

   <li>nDCG @ k</li>

  </ul></li>

 <li>Assume that for a given query, the set of relevant documents is as listed in <em>json</em>. Any document with a relevance score of 1 to 4 is considered as relevant. For each query in the Cranfield dataset, find the Precision, Recall, F-score, Average Precision and nDCG scores for k = 1 to 10. Average each measure over all queries and plot it as function of k. <strong>Code for plotting is part of the given template</strong>. You are expected to use the same. <strong>Report the graph with your observations based on it</strong>.</li>

 <li>Analyse the results of your search engine. Are there some queries for which the search engine’s performance is not as expected? Report your observations.</li>

 <li>Do you find any shortcoming(s) in using a Vector Space Model for IR? If yes, report them.</li>

 <li>While working with the Cranfield dataset, we ignored the titles of the documents. But, titles can sometimes be extremely informative in information retrieval, sometimes even more than the body. State a way to include the title while representing the document as a vector. What if we want to weigh the contribution of the title three times that of the document?</li>

 <li>Suppose we use bigrams instead of unigrams to index the documents, what would be its advantage(s) and/or disadvantage(s)?</li>

 <li>In the Cranfield dataset, we have relevance judgements given by the domain experts. In the absence of such relevance judgements, can you think of a way in which we can get relevance feedback from the user himself/herself? Ideally, we would like to keep the feedback process to be non-intrusive to the user. Hence, think of an ’implicit’ way of recording feedback from the users.</li>

</ol>