# BEQuizzer
This repository supports the paper BEQuizzer: AI-based Quiz Automatic Generation in the Portuguese Language, accepted paper by the NLDB 2024 conference. 


## Refined Models

We follow two main algorithm to finetune our models for generation:

**Algorithm 1** describes each fine-tunning approach for our question generator models using early stopping criteria with a patient of three focuses in ROUGE-1 metric. These criteria stop the fine-tuning process and save the best past configuration if our models do not create questions close to what is expected.
![](https://github.com/Studyard/BEQuizzer/blob/main/img/alg1.png?raw=true)

**Algorithm 2**

In algorithm 2, we used this pretrained to apply a fine-tuned process using instruction tunning to implement this configuration; the BeleBele dataset was used to this end. Similarly to algorithm 1, we used an early stopping three to stop the fine-tuning.

![](https://github.com/Studyard/BEQuizzer/blob/main/img/alg2.png?raw=true)
 
## LLMs
