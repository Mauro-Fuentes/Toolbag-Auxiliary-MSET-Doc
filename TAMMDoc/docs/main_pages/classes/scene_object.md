# Scene Object

class SceneObject

This is the base class from which all objects in the Scene deribe.

Subclases:
BackdropObject BakerObject BakerTargetObject FogObject RenderObject SkyBoxObject SubMeshObject TextureProjectObject TransformObject


### Instance Variables

<!-- ### var collapsed -->

```python
var collapsed
```

<p style="text-indent: 30px;">Controls the display of the object's children in the outline view.</p>

```python
var locked
```

<p style="text-indent: 30px;">Controls the display of the object's children in the outline view.</p>


```python
var name
```
```python
var parent
```
```python
var uid
```
```python
var visible
```

<!-- ### var locked -->

<!-- ## var name -->

<!-- ## var parent -->

<!-- ## var uid -->

<!-- ## var visible -->



```python title="example"
var collapsed
```


### Methods

```python
def destroy()
```

```python
def duplicate(name: str = '') ‑> SceneObject
```

```python
def findInChildren(searchStr: str) ‑> SceneObject
```

```python
def getBounds() ‑> List[List[float]]
```

```python
def getChildren() ‑> List[SceneObject]
```

```python
def setKeyframe(lerp: str)
```