# Call me green

## Description
This is just a green theme for Visual Studio Code. I made it for myself, but if you like it, feel free to use it.

## Installation

1. Open **Extensions** sidebar panel in VS Code. `View → Extensions`
2. Search for `Call me green`
3. Click **Install** to install it.
4. Click **Reload** to reload the your editor
5. Code > Preferences > Color Theme > **Call me green**

## Local Development

1. Clone the repository.
2. Open the folder in VS Code.
3. Press `F5` to launch an Extension Development Host.
4. In the new window, select **Call me green** from the Color Theme picker.

## Package Extension (VSIX)

1. Install packaging tooling:

```bash
npm install -g @vscode/vsce
```

2. Build a VSIX package:

```bash
vsce package
```

This generates a file like `callmegreen-0.0.10.vsix` that can be installed locally.

## Publish to VS Code Marketplace

1. Create a publisher access token in Azure DevOps with Marketplace manage scope.
2. Login once:

```bash
vsce login Callmesilva
```

3. Publish:

```bash
vsce publish
```

Or publish a specific version:

```bash
vsce publish 0.0.10
```

## Automated Publish With GitHub Actions

This repository includes [.github/workflows/publish-marketplace.yml](.github/workflows/publish-marketplace.yml), which publishes the extension when you push a version tag.

1. Create a Personal Access Token in Azure DevOps Marketplace with manage permissions.
2. Add it as a GitHub Actions repository secret named `VSCE_PAT`.
3. Ensure `package.json` version is updated (for example `0.0.11`).
4. Create and push a matching tag:

```bash
git checkout main
git pull --ff-only origin main
git tag v0.0.11
git push origin v0.0.11
```

The workflow validates that the tag version matches `package.json`, then runs `vsce publish`.

## Create a PR With Theme Changes

```bash
git checkout -b feat/vim-amber-palette
git add .
git commit -m "feat(theme): add vim-inspired amber palette and divider accents"
git push -u origin feat/vim-amber-palette
```

Then open a PR to `main` in GitHub.

## License

MIT License

Copyright 2023 Enrique Silva

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Peace.