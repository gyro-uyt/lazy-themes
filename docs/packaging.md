# Packaging the Lazy Themes Extension

This guide explains how to generate a `.vsix` file for the Lazy Themes extension after making changes.

## Prerequisites

- [Node.js](https://nodejs.org/) installed on your system.
- Standard terminal (Command Prompt, PowerShell, or Bash).

## Steps to Package

### 1. Update Version (Optional)
If you've made significant changes, update the version number in `package.json`.

1. Open `package.json`.
2. Update the `"version"` field (e.g., `0.1.3` to `0.1.4`).
3. Save the file.

### 2. Run Packaging Command
Run the following command in the root directory of the repository:

```bash
npx @vscode/vsce package
```

This command will:
- Validate your `package.json` for VS Code extension requirements.
- Bundle all necessary files.
- Create a `.vsix` file in the root directory named `lazy-themes-[version].vsix`.

### 3. Move to Release Folder
To keep your project clean and maintain a history of builds, move the generated `.vsix` file to the `release/` folder:

```bash
mv lazy-themes-*.vsix release/
```
*(On Windows PowerShell, use `move lazy-themes-*.vsix release/`)*

## Installation
To install the generated VSIX file in VS Code:
1. Open VS Code.
2. Go to the **Extensions** view (`Ctrl+Shift+X`).
3. Click the **...** (three dots) in the top-right corner.
4. Select **Install from VSIX...**.
5. Choose the newly generated `.vsix` file.
