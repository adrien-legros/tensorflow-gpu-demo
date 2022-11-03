# Using GPU on Openshift - Neural Network on Tensorflow

We aim to demonstrate the GPU utilization on an Openshift cluster. We will step by step go through a Jupyter Notebook that has all necessary packages installed. We will train a neural network in order to recognize pneumonia on chest xrays. You will see the resource usage thanks to the Grafana dashboards. Finally we will evaluate our model.

## Instructions

1. Open jupyterlab: https://tensorflow-gpu-test-odh.apps.sno-nvidia-p6.redhat.hpecic.net/notebook/test-odh/tensorflow-gpu/.
2. You will see on the left the file browser. Go to the *notebooks* directory. Create a personnal folder with your name and open it.
3. On the left you can see a *Git* icon. Click on it and clone this repository: https://github.com/adrien-legros/tensorflow-gpu-demo.
4. Go to the *tensorflow-gpu-demo* folder and open the *xray-tensorflow-NN.ipynb* notebook.
5. Keep in mind that 2 different dashboards are available here: https://grafana-route-grafana.apps.sno-nvidia-p6.redhat.hpecic.net/dashboards/ so you can observe the ressource consumption.
6. Run each cell step by step and refer to the instruction next to them.
