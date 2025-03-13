
# Export Functions

If you need to export something out of Toolbag, then these core functions will help you out.

It is essential to save files in custom folders instead of OS locations like the Desktop, which may have additional read and write permission restrictions. Normally, creating a folder is enough.

## exportViewer

‼️ERROR Is this not part of the API?

```python linenums="1" title="code"
def exportViewer(
                path: str = '',
                title: str = '',
                author: str = '',
                authorURL: str = '', 
                textureQuality: str = 'high',
                highResThumbnail: bool = False,
                html: bool = False,
                autoStartHTML: bool = False,
                fullframeHTML=False,
                presetHTML: bool = False,
                width: int = -1,
                height: int = -1,
                exportAnimations: bool = False,
                exportModelShowcase: bool = False,
                autoPlayAnimations: bool = False,
                showPlaybackControls: bool = False
                )
```

```python linenums="1" title="example"

def exportViewer(
                path: 'desktop',
                title: 'job',
                author: str = '',
                authorURL: str = '', 
                textureQuality: str = 'high',
                highResThumbnail: bool = False,
                html: bool = False,
                autoStartHTML: bool = False,
                fullframeHTML=False,
                presetHTML: bool = False,
                width: int = -1,
                height: int = -1,
                exportAnimations: bool = False,
                exportModelShowcase: bool = False,
                autoPlayAnimations: bool = False,
                showPlaybackControls: bool = False
                )
```


## exportSceneUSD

    exportSceneUSD(
        path: str = '',
        models: bool = True,
        lights: bool = True,
        skies: bool = True,
        cameras: bool = True,
        materials: bool = True,
        normals: bool = True,
        uvmaps: bool = True,
        vertexcolors: bool = True,
        triangulate: bool = False,
        subdivision: bool = False,
        displacement: bool = False,
        copyfilereferences: bool = False,
        skiptextures: bool = False,
        uniquetextures: bool = False )


SNIPPET

```python
import mset

def RunPlugin():
    mset.exportSceneUSD("G:\\Borrar", True, True, True, True, True, True, True,True, False, False, False, False, False, False)

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```


## exportSceneFBX


## exportSceneGLTF

## exportSceneOBJ

## exportSceneCOLLADA