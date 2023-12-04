# ML-Cyber-Security

# Data

Validation Data: bd_valid.h5 and valid.h5

Test Data: bd_test.h5 and test.h5

# Evaluating the Backdoored Model

The DNN architecture used to train the face recognition model is the state-of-the-art DeepID network. This DNN is backdoored with multiple triggers. Each trigger is associated with its own target label.

To evaluate the backdoored model, execute eval.py by running:
python3 eval.py <clean validation data directory> <model directory>.

E.g., python3 eval.py data/clean_validation_data.h5  models/sunglasses_bd_net.h5. Clean data classification accuracy on the provided validation dataset for sunglasses_bd_net.h5 is 97.87 %.

I could not upload data here as it is huge.

# The accuracy on clean test data 

Clean Classification accuracy: 98.64899974019225

# The attack success rate (on backdoored test data) as a function of the fraction of channels pruned.

![output](https://github.com/akanksha6/ML-Cyber-Security/assets/26012142/5a995881-40bd-4b52-916a-c3fb8cf6bb12)

# Performance of repaired networks

Your repaired networks are created by pruning the max pool layer and save the model when the accuracy drops.

model		      text_acc	  attack_rate
repaired_2%	  94.130943	  100.000000
repaired_4%	  94.130943	  100.000000
repaired_10%	74.247857	  100.000000
repaired_25%	64.232268	  99.992206

![repaired_model](https://github.com/akanksha6/ML-Cyber-Security/assets/26012142/e909cbd8-16d3-41e1-aeed-7e7e828fee5b)

# Performance of Goodnet (combined) model

We combine the repaired models with the bd model and evaluate the new models

G_model		G_text_acc	G_attack_rate
G_2%	    93.959470	  100.000000
G_4%	    93.959470	  100.000000
G_10%	    74.091972	  100.000000
G_25%	    64.123149	  99.992206

![goodnet_model](https://github.com/akanksha6/ML-Cyber-Security/assets/26012142/957fcf3c-a1ac-47a2-a3ff-1ad076435ae5)


