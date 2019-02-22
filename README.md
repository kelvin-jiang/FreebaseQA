# FreebaseQA - v1.0

This repository contains FreebaseQA, a new dataset for open-domain QA over the Freebase knowledge graph. The question-answer pairs in this dataset are collected from various sources, including the TriviaQA dataset ([Joshi et al., 2017](http://nlp.cs.washington.edu/triviaqa/)) and other trivia websites ([KnowQuiz](http://www.knowquiz.com), [QuizBalls](http://www.quizballs.com), and [QuizZone](https://www.quiz-zone.co.uk)), and are matched agaist Freebase to generate relevant subject-predicate-object triples that were further verified by human annotators. As all questions in FreebaseQA are composed independently for human contestants in various trivia-like competitions, this dataset shows richer linguistic variation and complexity than existing QA datasets, making it a good test-bed for emerging KB-QA systems.

If you find this dataset useful, please cite the paper:
> [1] K. Jiang, D. Wu and H. Jiang, "FreebaseQA: A New Factoid QA Dataset Matching Trivia-Style Question-Answer Pairs with Freebase," _Proc. of North American Chapter of the Association for Computational Linguistics (NAACL)_, June 2019. 

## Dataset Files

This dataset contains 28,348 unique questions that are divided into three subsets: `train` (20,358), `dev` (3,994) and `eval` (3,996), formatted as JSON files: `FreebaseQA-[train|dev|eval].json`.

Each file is formatted as follows:

* "Dataset" : The name of this dataset
* "Version" : The version of the FreebaseQA dataset
* "Questions" : The set of unique questions in this dataset
    * "Question-ID" : The unique ID of each question
    * "RawQuestion" : The original question collected from data sources
    * "ProcessedQuestion" : The question processed with some operations such as removal of trailing question mark and decapitalization
    * "Parses": The semantic parse(s) for the question
        * "Parse-Id" : The ID of each semantic parse
        * "PotentialTopicEntityMention": The potential topic entity mention in the question
        * "TopicEntityName" : The name or alias of the topic entity in the question from Freebase
        * "TopicEntityMid" : The Freebase MID of the topic entity in the question
        * "InferentialChain" : The path from the topic entity node to the answer node in Freebase, labelled as a predicate
        * "Answers" : 
            * "AnswersMid" : The Freebase MID of the answer
            * "AnswersName" : The answer string from the original question-answer pair

## Evaluation Metrics

The accuracy is used as the evaluation metric for this dataset, i.e. a question is considered correct only if the predicted answer is exactly the same as one of the given answers.

## Freebase Subset

We have created a subset of Freebase (2.2GB zip), which includes all relevant entities (16M) and triples (182M) to all FreebaseQA questions. The subset can accompany the FreebaseQA dataset in order to evaluate the accuracy of trained models in answering questions. The subset may be downloaded from the following link: [https://www.dropbox.com/sh/a25p7j2ir8gqnvx/AABJvjoI9mbHYj3hyfuxSdGaa?dl=0](https://www.dropbox.com/sh/a25p7j2ir8gqnvx/AABJvjoI9mbHYj3hyfuxSdGaa?dl=0)
