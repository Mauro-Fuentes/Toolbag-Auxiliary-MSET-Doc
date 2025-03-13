# IO Read and Write

This sections has all the functions that you need to save, write and load data in and out of Toolbag.



## loadScene

``` py 
def loadScene(filePath: str, downloadMissingLibraryAssets: bool = False)
```

Loads a Marmoset Toolbag scene file. Unsaved changes to any currently open scenes are lost.

## newScene

``` py 
def newScene()
```

Creates a new empty scene. Any unsaved changes in the current scene will be lost.

## quit

``` py 
def quit()
```

Quits Toolbag. Any unsaved changes will be lost.

## shutdownPlugin

``` py 
def shutdownPlugin()
```

Stops and shuts down the currently running plugin.

## saveScene

``` py 
def def saveScene(filePath: str)
```

Saves a Marmoset Toolbag scene file. If a scene file path is not specified, the scene will be saved to its existing location.

## importMaterial

## importModel

## freeUnusedResources