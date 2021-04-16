# A method to explain arbitrary machine learning classification models using human-assisted generated neighborhoods 

## Workflow of human user involvement
This method aims to improve explainability of machine learning models in a human-centric fashion. A human user or a software engineer can use it to understand why a given ML model misclassifies a data point. There are three human intervention points.

### Identifying the point-of-interest
First, the human user identifies a mispredicted point-of-interest, which software engineers routinely encounter as they debug software systems with ML components. 

### Identifying interesting dimensions and appropriate step lengths
Second, the key question from a user's perspective is: how and why a particular region of the point of interest is relevant to the prediction. That is where human users can again contribute by identifying the most interesting dimensions of semantic changes. Our framework leverages powerful generative models, variational autoencoders and GANs, to generate a neighborhood of closely related data points. The generated neighborhood displays a progressive set of plausible variations of the point-of-interest and visualizes the semantic changes across all directions. The human user can use his common sense judgement to identify more interesting dimensions and more appropriate step lengths of changes on these dimensions so that changes in neighboring data-points are perceivable but not too dramatic. 

### Selecting two most revealing dimensions to generate a matrix for decision boundary visualization
Third, human users then select two most revealing dimensions so that a matrix of data-points can be generated to visualize the efforts of gradual changes on both dimensions. This matrix represents the neighborhood of interest. All generated data-points in the neighborhood are passed through the actual model-under-investigation so that the decision boundary is identified and visualized verbatim. Human users can gain knowledge and insights by walking through the classified instances and examining the decision boundary. 

These three intervention points provide helpful exploration tools to help human users see, select, and manipulate the neighborhood of the data-point-of-interest and the decision boundary within it and therefore better understand the behavior of the underlying model. 

Three examples are provided in this repo to illustrate this method.
