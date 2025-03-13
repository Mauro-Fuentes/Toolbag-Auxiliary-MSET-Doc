
## Transform

This is the core module that all movable objects have. 
It stores the position of the object's coordinates in the world, and it is represented in the viewport with a gizmo.

It is the base class that allows objects to move in the viewport.

### Class

```python
class TransformObject(SceneObject):
```
<p style="text-indent: 30px;">Class for...</p>


### Instance variables


```c#
var pivot 
```
```c#
var position 
```
```c#
var rotation 
```
```c#
var scale 
```

### Methods

```python
def centerPivot():
```

<p style="text-indent: 30px;">Centers the pivot point of this object to its bounding box.</p>


## Camera
class CameraObject

## External Object
class ExternalObject

## Light
class LightObject

## Mesh
class MeshObject

## Turntable
class PyTurntableObject

## ShadowCatcher
class ShadowCatcherObject
