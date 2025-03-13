# Timeline

## getTimeline

def getTimeline() ‑> Timeline

Returns the current scene's timeline, for animation control.

```python
import mset

def RunPlugin():
    timeline = mset.getTimeline()
    
window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```
