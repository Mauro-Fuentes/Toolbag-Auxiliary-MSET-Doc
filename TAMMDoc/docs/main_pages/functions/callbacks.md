# Callbacks 


To better understand callbacks, you can think of the phrase "call me back"—meaning "contact me when something happens."  

In programming, a callback is like asking the program to notify you once a task or event is finished, so you don’t have to wait for it to complete.










<br>

<!-- ========== SECTION BREAK ========== -->











## onPeriodicUpdate

This callback runs periodically, a few times per second. 
This can be useful for plugins that need to refresh external files or make frequent checks. 
Since this callback runs frequently, be careful to keep the average execution time low.

<!--  ## var with background -->
 var <span style="background-color: #ededed;">onPeriodicUpdate</span>. 


```python
import mset

def doThis():
    print("I'm doing something all the time")

mset.callbacks.onPeriodicUpdate = doThis
```

With this code 👆 you can constantly call a 












<br>

<!-- ========== SECTION BREAK ========== -->












## onRegainFocus

This callback runs every time you come back to Toolbag.

```python
import mset

def doThis():
    print("Ooh, Toolbag regain focus")

mset.callbacks.onRegainFocus = doThis
```













<!-- ========== SECTION BREAK ========== -->













<br>

## onSceneChanged

This callback runs every single time you change something inside Toolbag.

```python
import mset

def doThis():
    print("Ooh, you just change something in Toolbag")
    
mset.callbacks.onSceneChanged = doThis
```













<br>

<!-- ========== SECTION BREAK ========== -->













## onSceneLoaded

This callback runs precisely when Toolbag finishes loading a scene.

```python
import mset

def doThis():
    print("This scene has been loaded")
    
mset.callbacks.onSceneLoaded = doThis
```












<br>



<!-- ========== SECTION BREAK ========== -->












## onShutdownPlugin


This callback runs exactly when the plugin is closed.

```python
import mset

def doThis():
    print("Uh-oh, your plugin is closed")
    
mset.callbacks.onShutdownPlugin = doThis
```
<br>











<!-- ========== SECTION BREAK ========== -->