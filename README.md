# IAR Embedded Workbench extension

This extension provides IAR Embedded Workbench project integration to automatize build and Intellisense support.
As IAR works on Windows environment only, the extension is not been tested on different systems.

This is NOT an official IAR Systems extension.

## Usage

After creating the `iar.json` file inside `.vscode` folder, make sure to enable the extension on your workspace or global settings (default `false`):

```javascript
{
    "iar.enabled":true
}
```

Then just run `ctrl+shift+b` to start build.

The extension automatically replaces your `c_cpp_properties.json` [Microsoft C++ Tools][cpptools] configuration to matches the IAR Project ones.
It supports browsing to external files, includepath, common defines and user included one.

## Configuration

Example `iar.json` configuration:
```javascript
{
    "version": 1,
    "path": "C:\\Program Files (x86)\\IAR Systems\\Embedded Workbench\\",
    "project": "C:\\Projects\\TEST\\TEST.ewp",
    "config": "Debug"
}
```
[cpptools]: https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools
