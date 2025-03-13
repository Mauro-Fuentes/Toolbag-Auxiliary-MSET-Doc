# Render Functions

Ready to render your art? 

These core core functions are designed so you can take a look at the final product of your art.


## setCamera

def setCamera(camera: CameraObject)

Selects the camera that you pass as the active one in the Viewport. This is the equivalent of selecting a camera using the dropdown menu in the Viewport.

Useful if you have a lot of cameras and you want to switch between them by code.


<!-- I don-t get this... the viewport camera is always the one from which we render Viewport Rendering_ -->


```python
import mset

def RunPlugin():
    cam = mset.getSelectedObject() #make sure to select a camera
    mset.setCamera(cam)

    print(cam.name)

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

<br>

By default, Viewport Rendering (F10) uses the current active camera in the Viewport as reference to render.
If you have more than one Viewport opened, then the last active one will be the reference.


<br>

## readAndExportStamp

Internal use by Marmoset's team for stamp brush creation.

def readAndExportStamp(inputPath: str, outputPath: str)  


<!-- «todo» -->

<br>

## renderCamera

Renders an image with the given camera with the current resolution/format settings from the render scene object.
If no camera is specified, the main camera will be used. 

ViewportPass accepts a render pass string (from component view / render passes dropdown box), if the string is not on the list or an empty string is used, the Full Quality pass is rendered by default.

Returns an mset.Image instance.

Optionally takes a path parameter which specifies where to write the image. If no path is specified, no image file will be written.

def renderCamera( 
    path: str = '',  
    width: int = -1,  
    height: int = -1,  
    sampling: int = -1,  
    transparency: bool = False,  
    camera: str = '',  
    viewportPass: str = '') ‑> Image


```python
import mset

def RunPlugin():
    mset.renderCamera( path = "C:\\Users\\Mauro Fuentes\\Desktop\\Test Code\\jon.png",  width= -1, height= -1,  sampling = -1, transparency= False,  camera = '',  viewportPass = '')

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

!! The path is optional because you may not be interested in saving the result to disk just yet, but to handle the raw data first.

!! The path needs to also contain the full name of the final file "C:\\Users\\Desktop\\Test Code\\MyRender.png"


```python
import mset

def RunPlugin():
    image_data = mset.renderCamera(camera="MyCamera")  # No path specified, so no file is saved

    if image_data:
        print("Image data exists!")
    else:
        print("No image data.")

    if image_data != b'':
        print("Image data has bytes!")
    else:
        print("No bytes in image data.")

    print(image_data)
    print(f"Type: {type(image_data)}")

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

<br>


## renderImages

Renders images with the render scene object's current settings and cameras. 
To render a single image, see renderCamera().

def renderImages (width: int = -1, height: int = -1, sampling: int = -1, transparency: bool = False)


<br>

## renderVideos

def renderVideos(width: int = -1, height: int = -1, sampling: int = -1, transparency: bool = False)

Captures an animation into a video file or image sequence. The animation will be written into the file path(s) specified in the scene's render object.

