# Using GPU on Openshift - Neural Network on Tensorflow

We aim to demonstrate the GPU utilization on an Openshift cluster. We will step by step go through a Jupyter Notebook that has all necessary packages installed. We will train a neural network in order to recognize pneumonia on chest xrays. You will see the resource usage thanks to the Grafana dashboards. Finally we will evaluate our model.

## Infrastucture

The following components has been installed on the Openshift cluster:
- [NVIDIA GPU Operator](https://console-openshift-console.apps.sno-nvidia-p6.redhat.hpecic.net/k8s/ns/nvidia-gpu-operator/operators.coreos.com~v1alpha1~ClusterServiceVersion/gpu-operator-certified.v22.9.0) on nvidia-gpu-operator namespace
- [Node Feature Discovery Operator](https://console-openshift-console.apps.sno-nvidia-p6.redhat.hpecic.net/k8s/ns/openshift-nfd/operators.coreos.com~v1alpha1~ClusterServiceVersion/nfd.4.11.0-202210251429) on openshift-nfd
- [Open Data Hub Operator](https://console-openshift-console.apps.sno-nvidia-p6.redhat.hpecic.net/k8s/ns/openshift-operators/operators.coreos.com~v1alpha1~ClusterServiceVersion/opendatahub-operator.v1.4.0) with a KfDek instance in test-odh namespace

The lab you will run will be on jupyterlab. You still have access to the deployed resources on the following urls.

Please refer to this gihub url if you want to reproduce the lab: https://github.com/adrien-legros/tensorflow-gpu-deploy.

## Credentials

You can connect to the Openshift console or CLI:

Openshift console url: https://console-openshift-console.apps.sno-nvidia-p6.redhat.hpecic.net  
Openshift server url: https://api.sno-nvidia-p6.redhat.hpecic.net:6443 

## Lab instructions

We propose you this lab as an example of GPU utilization. However you are free to create another notebook.

1. Open jupyterlab: https://tensorflow-gpu-test-odh.apps.sno-nvidia-p6.redhat.hpecic.net/notebook/test-odh/tensorflow-gpu/.
2. You will see on the left the file browser. Go to the *notebooks* directory. Create a personnal folder with your name and open it.
3. On the left you can see a *Git* icon. Click on it and clone this repository: https://github.com/adrien-legros/tensorflow-gpu-demo.
4. Go to the *tensorflow-gpu-demo* folder and open the *xray-tensorflow-NN.ipynb* notebook.
5. Keep in mind that 2 different dashboards are available here: https://grafana-route-grafana.apps.sno-nvidia-p6.redhat.hpecic.net/dashboards/ so you can observe the ressource consumption.
6. Run each cell step by step and refer to the instruction next to them.