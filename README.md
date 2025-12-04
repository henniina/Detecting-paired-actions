# Detecting-paired-actions
<img width="520" height="400" alt="illustr2" src="https://github.com/user-attachments/assets/b3653165-6c0d-433f-8d9a-6f949f5c8e60" />

This repository provides resources developed for the identification of face-threatening and paired actions in asynchronous social media discussions and comments to crisis-related news.
The annotation framework and guidelines can be used for implementing novel classification approaches to also other contexts (e.g., different language or platform contexts), but in these cases the framework should be tested and refined in case other important actions emerge as important (other than what we used).

## Resources:
- **Models:** Models can be found here: https://huggingface.co/Finnish-actions
- **Paper:** Paakki, H., Toivanen, P. and Kajava K. (2025). Implicit and Indirect: Detecting Face-threatening and Paired Actions in Asynchronous Online Conversations. _Northern European Journal of Language Technology (NEJLT)_, 11(1), pp. 58-83.
- **Data:** If you wish to replicate our study or use our data for research purposes (abiding by rules stated here), please get in touch.



## Classes in our framework:
```
- Question* : Asks someone for information (request for information)
- Request* : Requests, proposes, or tells someone to perform an action.
- Challenge* : Refutes someone’s acceptance,epistemic claim or authority.
- Accusation* : Points out a reprehensible act performed by someone.
- Statement : Asserts an opinion, information, wish, neutral or negative evaluation, or answer (to question).
- Appreciation : Positive evaluation or comment about an actor, event or object.
- Acceptance : Agrees, or accepts a request, statement or challenge, or admits an accusation.
- Denial : Rejects or denies an action.
```
*Action expects a response.

## Framework and model application

### Downstream Use

These models have been trained on data coming from Finnish language asynchronous conversations under crisis related news on Facebook.
They have been trained to detect whether a comment includes an action or not. Some of the models reflect only one of our annotators' label interpretations, so the best use of our models (see our paper) would be to combine a set of models we provide on our Huggingface (Finnish-actions), and use a model ensemble to provide label predictions.
It needs to be noted also that the models may not be well applicable outside of their empirical context, so in downstream applications, one should always conduct an evaluation of the model applicability using manually annotated data from that specific context (see our paper for annotation instructions).

### Out-of-Scope Use

Please use our models only for action detection and analysis.
Uses of the models and the involved data for generative purposes (e.g. NLG) is prohibited.

### Bias, Risks and Limitations

Note that the models may produce errors. Due to the size of the training dataset, models may not generalize very well even for other novel topics within the same context.
Note that model predictions should not be regarded as final judgments e.g. for online moderation purposes, but each case should also be regarded individually if using model predictions to support moderation.
Also, the annotations only reflect three (though experienced) annotators' interpretations, so there might be perspectives on data intepretation that have not been taken into account here.

If model is used to support moderation on social media, we recommend that final judgments should always be left for human moderators.


## Citation

If you use this model, please cite the following work:

### BibTeX
```bibtex
@article{paakki-implicit-indirect,
    doi = {https://doi.org/10.3384/nejlt.2000-1533.2025.5980},
    url = {https://nejlt.ep.liu.se/article/view/5980},
    author = {Paakki, Henna and Toivanen, Pihla and Kajava, Kaisla},
    title = {Implicit and Indirect: Detecting Face-threatening and Paired Actions in Asynchronous Online Conversations},
    publisher = {Northern European Journal of Language Technology (NEJLT)},
    volume= {11},
    number= {1},
    year = {2025}
}
```

<!-- copyright = {Creative Commons Attribution 4.0 International}
