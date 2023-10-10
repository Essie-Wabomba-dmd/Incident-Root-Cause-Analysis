### Incident-Root-Cause-Analysis

**Problem Statement**
Using data about CPU load, memory load, network delays, and three types of errors, build a model to predict the root cause of error. 

A data center team wants to buid a model that predicts causes of issues reported by customers.
They use a system monitoring tool to track CPU, memory and application latency for all their services.
They also track specific errors reported by applications

- Use the information Given to predict the root cause of the issue noticed
- A dataset is available for each incident, indicating if any load issues or errors was observed during that time
- Target variable is the root cause
- Incident Reports in ITOps usually states the symptoms. Identifying the root cause of the symptom quickly is a key determinant to reducing resolution times and improving user satisfaction.

### Preprocessing Incident Data
- Loading the Dataset and explore the data.

### Convert data
- Input data needs to be converted to formats that can be consumed by ML algorithms
- All the values for the feature variables are either 0, 1 hence already normalized, no further processing is required, we simply need to convert the data to a numpy array of float numbers.
- For target variables, we use one hot encoding.
- We then split the data into training and test data to get data ready for deep learning

### Building and evaluating the model
  - Setup Training Parameters
  - Create a Keras sequential model
  - Add a Dense Layer
  - Add a second dense layer
  - Add a softmax layer for categorical prediction
  - Compile the model
  - Build the model
  - Evaluate the model against the test dataset and print results

### Predicting Root Causes
- Pass individual flags to predict the root cause
- Predicting as a Batch
