---
description: How to package the VS Code extension into a VSIX file
---

This workflow automates the generation of a `.vsix` package for the extension.

1. Ensure all changes are saved and the version in `package.json` is correct.
// turbo
2. Generate the VSIX package and move to release folder
```powershell
npx @vscode/vsce package
move lazy-themes-*.vsix release/
```

The resulting file will be stored in the `release/` directory.
