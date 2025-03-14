COMP90086 project

Please place the train.csv, test.csv, test folder, train folder in the same dir as this juypter notebook.

Project purpose: Design a method to predict the stability of a stack of blocks from a single image.

Data Preprocessing：
Execute the first 8 code cells of the jupyter notebook in order
This includes importing training and test data, data preprocessing in the first stage, and data splitting and preprocessing in the second stage.

Baseline comparison (phase 1)：
1.	Execute vitmodel, inceptionv4model, resnetmodel and mobilemodel.
2.	Execute loss function weight allocation
3.	Execute function stable_height_validate(model, eval_loader), used to evaluate the performance of the model on the validation set
4.	Perform different model training in sequence
5.	Execute function modeltraining(model,savepath,log) for each model in turn. Note that savepath is the weight of the saved model, and log is the data result of the training model (on tensorboard)
6.	Execute function modelpredict(model, save_path) for each model in turn:
7.	Input  %load_ext tensorboard and %tensorboard --logdir=runs to open tensorboard to view the training and validation results of all models.

Improved model(phase 2)
1.	Execute model1 as instability_type_model
2.	Training model1
3.	Execute model2 and use model2 to define type_0_model, type_1_model, type_2_mode
4.	Train three models separately
5.	Execute function predict(model, save_path) to predict the instability type for each test image
6.	Execute function predict(model, save_path, loader) to predict the stable height for each type
7.	Combine the prediction results of each type and sort them according to the order of the ids in test dataset

All experiments can be completed by executing jupyter notebook in sequence
