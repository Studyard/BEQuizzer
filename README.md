# BEQuizzer
This repository supports the paper BEQuizzer: AI-based Quiz Automatic Generation in the Portuguese Language, accepted paper by the NLDB 2024 conference. 


## Refined Models

We follow two main algorithm to finetune our models for generation:
 
**Algorithm 1** describes each fine-tunning approach for our question generator models using early stopping criteria with a patient of three focuses in ROUGE-1 metric. These criteria stop the fine-tuning process and save the best past configuration if our models do not create questions close to what is expected.

![](https://github.com/Studyard/BEQuizzer/blob/main/img/alg1.png?raw=true)

**Algorithm 2** pretrained to apply a fine-tuned process using instruction tunning to implement this configuration; the BeleBele dataset was used to this end. Similarly to algorithm 1, we used an early stopping three to stop the fine-tuning.

![](https://github.com/Studyard/BEQuizzer/blob/main/img/alg2.png?raw=true)
 
## LLMs


In the following, we present an example (translated by the authors from Brazilian Portuguese) of our designed prompt used in our article:

```
You are a professor working on quizzes. Given the following document, please generate a multiple-choice question with five possible choices and one letter corresponding to the correct one.

(Format instructions generated in English by LangChain's {ResponseSchema})

(Begin document)

*Document omitted due to space*

(End document)
```

This prompt can be easily changed to accommodate the generation of more questions for the same input text and an arbitrary number of choices while reducing the number of calls to the model's API.