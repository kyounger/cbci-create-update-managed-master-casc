# CloudBees CI: Create Managed Masters Programmatically

## `create-update-managed-master-no-casc.groovy`

This script shows how to programmatically create/update a managed master. You can specify the provisioning details.

## `create-update-managed-master.groovy`

This script will create/update a managed master and a corresponding casc bundle based on a `masterName` and a yaml `masterDefinition` of the master.

The yaml definition is just a conjoined data structure of the various casc bundle files (`jenkins.yaml`, `plugins.yaml`, and `plugin-catalog.yaml`, and a `provisioning` section that can take any property assignable through the master provisioning process.

Note that the script manages the creation of the entire casc bundle on the OC, which includes the `bundle.yaml` file and its version. You do not need to manage casc bundles if you use this!!!

## `create-update-managed-master-with-state.groovy`

This additional script shows how to persist a representation of the masterDefinition to disk. The script then checks if the state differs before updating and restarting a master. Turns the script into a no-op if there are no changes to the master.

### P.S.

These are cut down (and self-contained) example scripts. If you find this appealing, it might be worth looking at the [more encompassing solution](https://github.com/kyounger/cbci-helmfile) that allows you to specify multiple masters in a grander yaml strucure in a configmap.
