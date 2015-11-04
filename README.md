# kevoree-dotnet
A Kevoree runtime for the .net framework

## Running a model
The Kevoree Runtime for the .NET platform is available at https://github.com/kevoree/kevoree-dotnet-core-bootstrap/releases

### Installation
 1. Download the [kevoree-core-bootstrap.zip](https://github.com/kevoree/kevoree-dotnet-core-bootstrap/releases/latest) archive and extract it.
 2. Add kevoree-dotnet-core-bootstrap.exe to the PATH.

### Execution
Executing kevoree-dotnet-core-bootstrap.exe without arguments starts a default model.

Default model in KevScript :
```
add node0 : DotnetNode
add sync : WSGroup
attach node0 sync
```
It looks for the latest DotnetNode and WSGroup in the registry and link them.

## Publishing a component to the registry

The Kevoree Runtime for the .NET platform is available at https://github.com/kevoree/kevoree-dotnet-model-generator/releases

### Installation
1. Download the [kevoree-model-generator.zip](https://github.com/kevoree/kevoree-dotnet-model-generator/releases/latest) archive and extract it.
2. Add kevoree-dotnet-model-generator.exe to the PATH.

### Publication

The minimal publication command require 5 arguments.
 * **package.name** and **package.version** defines the Nuget package to publish.
 * **typeDef.name**, **typeDef.version** and **typeDef.package** defines the informations about the Type Definition of the *dotnet* Deploy Unit you want to publish.

```
.\kevoree-dotnet-model-generator.exe --package.name=%NUGET_PACKAGE_NAME% --package.version=%NUGET_PACKAGE_VERSION% --typeDef.name=%KEVOREE_COMPONENT_NAME% --typeDef.version=%KEVOREE_COMPONENT_VERSION% --typeDef.package=%KEVOREE_COMPONENT_PACKAGE%
```
