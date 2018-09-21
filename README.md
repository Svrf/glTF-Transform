# glTF-Split

> **NOTICE:** Experimental and incomplete.

Splits a glTF file, so that separate meshes are in separate bin files.

## Installation

```
npm i -g gltf-split
```

## Usage

```
Usage: gltf-split [options] <file>

Options:

  -V, --version          output the version number
  -o, --output <file>    output filename
  -p, --prettyprint      prettyprint JSON
  -m, --meshes <meshes>  comma-delimited mesh names to separate
  -h, --help             output usage information
```

Example:

```
gltf-split original.gltf --output split/split.gltf --meshes MeshA,MeshB
```

## Status

Limitations:

- All meshes in the original mesh must use separate buffer views.
- All buffers in the original mesh must use Data URIs.
- Embedded images are not supported.
- Binary (.glb) files are not supported.
