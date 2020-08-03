# Create managed masters programmatically

## create-update-managed-master.groovy

This script will create a managed master and a corresponding casc bundle based on a masterName and a yaml definition of the master.

The yaml definition is just a conjoined data structure of the various bundle.yaml files, and a provisioning node that can take any property assignable through the master provisioning process.

Note that the script manages the creation of the `bundle.yaml` file and the version of it.

## create-update-managed-master-with-state.groovy

This additional script shows how to persist a representation of the masterDefinition to disk and check if the state differs before updating.

### P.S.

These are cut down (and self-contained) example scripts. If you find this appealing, it might be worth looking at the [more encompassing solution](https://github.com/kyounger/cbci-helmfile) that allows you to specify multiple masters in a grander yaml strucure in a configmap.
