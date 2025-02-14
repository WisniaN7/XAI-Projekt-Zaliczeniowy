# LLaVA Explainer overview
[Step-by-step conclusions jupyter notebook](https://github.com/WisniaN7/XAI-Projekt-Zaliczeniowy/blob/main/LLaVA/LLaVA.ipynb)

## TL;DL
* LLaVA seems to be designed with user friendly(-ish) approach first, where primary use case scenario is starting up a worker service with a browser interface.
  
![{76228BD5-4F64-425D-A9D6-FB7F629B1D56}](https://github.com/user-attachments/assets/6a3e420f-115a-4e35-98fd-3b2569255ee0)

* The code example provided on the repository is a good start, but works only once due to some bug, that breaks the `load_pretrained_model` function when run more than once. (Section ``Jumping through hoops to get rid of errors when using load_pretrained_model more than once``.
* LLaVA was fed a prompt asking to provide a explanation of a different model's classification based of of a sailency map.
* The explanations given by LLaVA were nothing spectacular, mostly pointing out obvious things.
* The bleeding of most important regions on sailency maps often caused LLaVA to put too much importance on things not related to classification at all (model T with an old man example).
* Not once the explanations pointed out someting not trivial, like in the train and a bridge example, where image classified as `steel arch bridge` contained a bridge that was neither a steel, nor an arch bridge.
