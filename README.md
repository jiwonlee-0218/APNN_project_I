# APNN_project_I
This project is for application and practice in neural networks



# The object of project
The objective of this project is to assess how effectively the transformer can embed fMRI signals.


# Dataset description
+ Training Data (train_hcp-task.pth):
  + Comprises a total of 5,944 subjects.
  + We used AAL (116) ROIs.
  + 7 main tasks: emotion (831, 176, 116), gambling (873, 253, 116), language (835, 316, 116), motor (868, 284, 116), relational (828, 232, 116), social (837, 274, 116), and working memory (872, 405, 116).
  + Each main task has associated sub-task labels, detailing activities at each time point.
  + The data is further split using a train-test split method to create a validation set.
+ Testing Data (test_hcp-task.pth):
  + Consists of 1,484 subjects for sub task prediction.
 

# Model description
In the first stage, we pretrain a transformer-based autoencoder to learn the embedding.
In the second stage, we fix the pretrained model and obtain embedding for each time point.
In the last stage, the embedding is then input into a classifier consisting of two fully-connected layers.
