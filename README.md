# KRVQA

## Dataset


The "question_answer_reason.json" is the generated QA samples. It contains a list of question-answer samples. Each sample has the following field:

* "question": The question raw text.
* "answer": The answer raw text.
* "level": The inference step of this question.
* "KB": 0 or 1 that indicates whether this question is generated with extern knowledge base.
* "qtype": The question type described in the paper.
* "reason": A list that contains the used scene graph triplets from Visual Genome or knowledge triplets from FVQA("all_fact_triples_release.json").
* "image_id": The image id from Visual Genome.
* "question_id": The ID question of this question.

The "splits.json" contains questions' ID for our train/val/test split. It has the following keys:

* "train": a list of training "question_id"
* "val":   a list of validation "question_id"
* "test":  a list of test "question_id"

The images, their feature and their scene graph annoation can be downloaded from [Visual Genome official website](http://visualgenome.org/).

The extern knowledge based is provided by FVQA[1], and can be downloaded from [dropbox](https://www.dropbox.com/s/iyz6l7jhbt6jb7q/new_dataset_release.zip?dl=0). We use the "new_dataset_release/all_fact_triples_release.json" as the complete extern knowledge base.

## References

[1] P. Wang, Q. Wu, et al. "FVQA: Fact-based visual question answering", 
IEEE Transactions on Pattern Analysis and Machine Intelligence, 2017
