The aim of this project is to provide a practical example of Transfer Learning:

In the specific of model merging we will focus on Multi-task learning (MTL), technique that enables the transfer of knowledge among multiple tasks by efficiently sharing model parameters , exploring methodologies for effectively merging multiple independently fine-tuned models, with the goal of improve performances across a variety of tasks.
We use as model backbone for feature extraction ModelNetV2, a light weight model suitable for Image Classification developed by Google. It is tipical used in mobile devices and strongly reduce the complexity cost and model size of the network wrt other models like VIT for example.
In MNV2 the first block perform a depthwise convolution and the second use a fully connected (1x1 convolution) which is responsible for building new features through computing linear combinations of the input channels.
Tasks & Merging:
Initially the model it's been fine-tuned onto two distinct tasks to perform classification of human vs horses and subsequently cat vs dogs. Those datasets are not very challenging but we will test the model merging behaviour onto new different task (EuroSAT, that contains images of 10 different satellitar images subjects) and take a look to the behaviour onto already seen data after the merging step. We performed Model Arithmetic technique with learning by addition and Ada Merging.
