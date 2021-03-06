### Overview

This application takes a ubuntu image that has python, bash, curl and tar installed (these are prerequisites for KD - see [here](https://github.com/bluek8s/kubedirector/wiki/App-Definition-Authoring-for-KubeDirector)).

The main focus point for this application is the use of a config package:

```
...
"defaultConfigPackage": {
   "packageURL": "https://github.com/hpe-container-platform-community/kubedirector-examples/releases/download/release/02-config-package-appconfig.tgz"
},
...
```

You can find the config package in the [appconfig](./appconfig) folder in this repo.

The config package is built and uploaded as a release [artifact](https://github.com/hpe-container-platform-community/kubedirector-examples/releases/download/refs%2Fheads%2Fmain/02-config-package-appconfig.tgz) to this github repo using github [actions](https://github.com/hpe-container-platform-community/kubedirector-examples/blob/main/.github/workflows/upload_asset.yml).

### Create the KubeDirectorApplication

Refer to [01-hello-world](https://github.com/hpe-container-platform-community/kubedirector-examples/tree/main/01-hello-world) instructions if you need a reminder.

### Create a KubeDirectorCluster

Refer to [01-hello-world](https://github.com/hpe-container-platform-community/kubedirector-examples/tree/main/01-hello-world) instructions if you need a reminder.

### Test the new KubeDirectorCluster

Access the service endpoint with a web browser and observe what is displayed.

### Exercises

1. Fork this repository.
2. Modify the startscript to print your name in the output.
3. Commit your changes.  You should see the github action building.
4. Redeploy and test.
