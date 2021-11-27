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
