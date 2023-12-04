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

![repaired_model](https://github.com/akanksha6/ML-Cyber-Security/assets/26012142/e909cbd8-16d3-41e1-aeed-7e7e828fee5b)

# Performance of Goodnet (combined) model

![goodnet_model](https://github.com/akanksha6/ML-Cyber-Security/assets/26012142/957fcf3c-a1ac-47a2-a3ff-1ad076435ae5)


