# Bake

One of Toolbag’s core functions is baking.

**Baking** is the process of *precomputing complex calculations*—such as lighting, shadows, and material details—and storing them in textures. This optimization *reduces real-time processing demands*, freeing up system resources.

In this sense, *baking is the opposite of real-time rendering*, where these calculations happen dynamically.

<br>

## BakeAll

```python title="code"
def bakeAll()
```

BakeAll will parse all **Bake Projects** in the Scene and bake all selected maps.




``` py linenums="1" title="example"
import mset

def RunPlugin():
    mset.bakeAll()
    
window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

