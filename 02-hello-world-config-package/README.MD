### Overview

This application extends 01-hello-world adding a config package:

```
...
"defaultConfigPackage": {
   "packageURL": "https://github.com/hpe-container-platform-community/kubedirector-examples/releases/download/refs%2Fheads%2Fmain/02-hello-world-config-package-appconfig.tgz"
},
...
```

The config package is built and uploaded so that it is available at the above url using using a [github action](https://github.com/hpe-container-platform-community/kubedirector-examples/blob/main/.github/workflows/upload_asset.yml).

The config package can be found in the folder [appconfig](https://github.com/hpe-container-platform-community/kubedirector-examples/tree/main/02-hello-world-config-package/appconfig) in this repository.

The [startscript](https://github.com/hpe-container-platform-community/kubedirector-examples/blob/main/02-hello-world-config-package/appconfig/startscript) is run when the application is provisioned.

If we look inside a running instance of the docker container, we see something like this:

```bash
root@7dd5d37742f8:/www# cat /www/index.html
<html><head><title>HTTP Hello World</title></head><body><h1>Hello from 7dd5d37742f8-config-package</h1></body></html
```

At the end of our startscript we have the following line:

```bash
sed -i s/$(hostname)/$(hostname)-config-package/ /www/index.html
```

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
