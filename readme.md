# A Collection of purpose-built devcontainers

As a way to package devcontainers and features into one container, each individual devcontainer will container the features
that are specified by the respective /src/{container}/devcontainer.json file and contents

## Using this repository

Build a devcontainer using
``` sh
# from src/{container}
devcontainer build --workspace-folder .     
```
