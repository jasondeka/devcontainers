# Devcontainers

This is a collection of specific devcontainers, complete with features, that can be consumed as-is within a development project

## Installation

Locally: 
---
Install the developer cli

DevContainer (VSCode):
---
Re-open the project inside of the included devcontainer

## Usage

See: .vscode *.code-snippets for project-wide snippets

Build and test a devcontainer locally:

``` sh
# Test the image
export REGISTRY=ghcr.io
export USERNAME=jasondeka
export IMAGE_NAME=devcontainer-go-hugo
export VERSION=v0.0.1
export IMAGE_NAME=$REGISTRY/$USERNAME/$IMAGE_NAME:$VERSION
export SRC_FOLDER=./src/go-hugo
devcontainer build --workspace-folder $SRC_FOLDER --image-name=$IMAGE_NAME

# Push the image
export CR_PAT=$(cat ~/.dev-secrets/.ghc-rdevcontainer-push) ; echo $CR_PAT | docker login $REGISTRY -u $USERNAME --password-stdin

devcontainer build --workspace-folder $SRC_FOLDER --push true --image-name=$IMAGE_NAME
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

Copyright (C) Slalom Consulting - All Rights Reserved
Unauthorized copying of this file, via any medium is strictly prohibited
Proprietary and confidential
