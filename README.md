# FreebaseQA v1.1

> `wc *.???`  
    7676   184416  1429963 `FreebaseQA-dev.tab`  
    4011    64738   373613 `FreebaseQA-dev.txt`  
    7655   182992  1419695 `FreebaseQA-eval.tab`  
    4023    65533   378217 `FreebaseQA-eval.txt`  
	39279   944728  7316479 `FreebaseQA-train.tab`  
	22792   554602  4333450 `QA-partialrelevant.tab`  

* `FreebaseQA-train.tab`: the training set of Q/A pairs and their corresponding Freebase IDs and predicates; the tab-separated fields are defined as follows:

    field 1 - the subject found in the question  
    field 2 - the freebase name corresponding to the subject  
    field 3 - the freebase ID corresponding to the subject  
    field 4 - the matched freebase predicate  
    field 5 - the secondary predicate for a mediator node (null	otherwise)  
    field 6 - the freebase mid corresponding to the answer  
    field 7 - the answer to the question  
    field 8 - the question  

* `FreebaseQA-dev.tab`: the development set of Q/A pairs and their corresponding Freebase IDs and predicates; the format is the same as `FreebaseQA-train.tab` as above

* `FreebaseQA-eval.tab`: the evaluation set of Q/A pairs and their corresponding Freebase IDs and predicates; the format is the same as `FreebaseQA-train.tab` as above

* `FreebaseQA-dev.txt`: the development set of 4011 Q/A pairs (separated by '|') from 3995 unique questions

* `FreebaseQA-eval.txt`: the evaluation set of 4023 Q/A pairs (separated by '|') from 3999 unique questions

* `QA-partialrelevant.tab`: all Q/A pairs and their corresponding Freebase IDs and predicates ONLY partially relevant to the questions; the format is the same as `FreebaseQA-train.tab` as above
