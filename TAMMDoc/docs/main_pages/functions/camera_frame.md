# Camera

These two independant functions should not be confused with the camera itself.

These are just two handy high-order functions for quickly setting up the camera.

## frame Object

```python title="code"
def frameObject(object: SceneObject)
```

This function Adjusts the active camera to frame the object, making it fully visible and centered in the viewport.

```python title="example"
import mset

def RunPlugin():
    object = mset.getSelectedObject() #make sure to select an object
    mset.frameObject(object)

    print(cam.name)

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

## frame Scene

```python title="code"
def frameScene()
```

Centers and frames the entire scene in the current camera.

Notice, you don't need to specify any object, because Toolbag calculates the bounds of the scene automatically.


```python title="example"
import mset

def RunPlugin():
    mset.frameScene()

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```