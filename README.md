# rhoai-inference-only

Configure Red Hat OpenShift AI to only serve models for inference

This is based on the [Red Hat OpenShift AI CLI Component Install Documentation](https://docs.redhat.com/en/documentation/red_hat_openshift_ai_self-managed/2.15/html/installing_and_uninstalling_openshift_ai_self-managed/installing-and-deploying-openshift-ai_install#installing-and-managing-openshift-ai-components_component-install) combined with the [Preparing RHOAI for IBM CloudPak for Data Documentation](https://docs.redhat.com/en/documentation/red_hat_openshift_ai_self-managed/2.13/html/installing_and_uninstalling_openshift_ai_self-managed/preparing-openshift-ai-for-ibm-cpd_prepare-openshift-ai-ibm-cpd).

# How to install

## Step 1 - Login

```sh
oc login <openshift_cluster_url> -u <admin_username> -p <password>
```


## Step 2 - Install the RHODS Operator

```sh
oc apply ./00-install-rhods-operator.yaml
```

## Step 3 - Create the DSCInitialization CR

```sh
oc apply ./01-create-rhods-dsc.yaml
```

## Step 4 - Create the DataScienceCluster CR

```sh
oc apply ./02-create-rhods-dsci.yaml
```
