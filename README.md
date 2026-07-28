# deploy-action

> You can use this action autho-deploy your Dioxus web project.

```yml
name: github pages

on:
  push:
    branches:
      - main

jobs:
  build-deploy:
    runs-on: ubuntu-latest
    permissions:
      contents: write

    steps:
      - name: "Dioxus Deploy"
        uses: Thierry61/deploy-action@1.0
        with:
          buildMode: release
          toolchain: stable
          outDirectory: dist
          rootPath: .
```
