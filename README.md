# SAE4K
Structured Argument Extraction for Korean

### Scheme at a glance<br/>
<image src="https://github.com/warnikchow/sae4k/blob/master/fig1.PNG" width="500"><br/>

## Summary
### This is an annotation guideline for the Korean questions and commands that are possibly non-canonical and highly conversation-style.
For the questions, the effective question set is obtained, and for the commands, the to-do-list is extracted; we call these **arguments**. The extraction process is not rule-based and fully manual for the corpus generation. The concept is slightly difference from slot-filling since the utterances are non-domain-specific and some contain inappropriate terms for the conventional dialog managers. We aim extracting the arguments from those utterances in a structured format.
### The extraction process does not base on just entity recognition; it converts the wh-particles or requrements into the lexicon that is proper.
For instance, for two questions "When will rain stop" and "When are you going vacation", the former asks for the time or period, while the latter asks for the day, week or month. We utilize various wh- related nouns to extract the question set appropriately. The similar holds for the commands, from requirements to the order-related lexicon.
### The extraction process omits the components that are not necessary for the content.
In Korean, and possibly for many other languages, not all the words (or particles) in the sentence may be necessary for the extraction of the arguments. For such non-canonical directive utterances, words or particles that are not appropriate to be included in the argument, are removed considering the semantics. This might convert a noisy input utterance into the format that let dialogue managers label the semantic roles more easily.
#### An additional dataset construction and the computational approach is in progress; will be disclosed with a paper.

## Corpus Description
### Questions - [Question-Argument] pairs w/ question type label
- Yes/no (label 0): 5,718 (31.99%)
- Alternative (label 1): 227 (1.27%)
- Wh- (label 2): 11,924 (66.73%)
### Commands - [Command-Argument] pairs w/ negativeness label
- Prohibition (label 3): 477 (3.67%)
- Requirement (label 4): 12,369 (95.38%)
- Strong requirement (label 5): 122 (0.94%)

## Citation
- W. I. Cho, Y. K. Moon, W. H. Kang, and N. S. Kim, "Extracting arguments from Korean question and command: An annotated corpus for structured paraphrasing," arXiv:1810.04631, Oct. 2018. [[paper]](https://arxiv.org/abs/1810.04631)

```
@article{cho2018extracting,
  title={Extracting Arguments from Korean Question and Command: An Annotated Corpus for Structured Paraphrasing},
  author={Cho, Won Ik and Moon, Young Ki and Kang, Woo Hyun and Kim, Nam Soo},
  journal={arXiv preprint arXiv:1810.04631},
  year={2018}
}
```
