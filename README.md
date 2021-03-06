# workspace-pack

Create a deployable npm package when using Yarn workspaces

## Details

If you use Yarn's `workspaces` feature to manage a monorepo, but need to "pack" a single package into a deployable zip that resolves both local and remote dependencies, this might be the tool for you.

## Install

```
$ yarn global add @bubuntux/workspace-lambda-pack
```

## Usage

```bash
# In your workspaces root dir
$ workspace-pack my-package-folder
```
or
```bash
# In your workspace dir
$ workspace-pack --root-dir=../../
```


## Options

| CLI arg       | Description                                                                                      |
| ------------- | ------------------------------------------------------------------------------------------------ |
| `--root-dir`  | Specify where the root package with the workspaces is located (useful when executing from the workspace) |
| `--build-dir` | Specify where the prepared package is created before it is built and zipped. _Default: `_build`_ |
| `--out-dir`   | Directory of the resulting .zip file. _Default: `dir`_                         |
| `--zip-name`  | Name of the resulting .zip file. _Default: `${package.name}.zip`_                         |
