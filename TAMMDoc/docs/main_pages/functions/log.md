# Log

Keep records of the events or activities of the system or your plugin.

<br>

## log

Prints text in the console.
It is similar to print().

def log (msg: str)


```python
import mset

def RunPlugin():
    mset.log ("\nThis is the message I wanted to log ")

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

<br>

## err

Prints text in the console, but as an error.

The core difference with **log** is that if you are not filtering Show Only Errors, you won't see the message error, and viseversa.
This is useful when you are debugging.

def err (msg: str)

```python
import mset

def RunPlugin():
    mset.err ("\nThis message is an error ")

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

<br>

## fail

Prints text directly to the log.txt Toolbag's internal file. It's mainly for internal use.

```python
import mset

def RunPlugin():
    mset.fail ("\nThis message will appear in the log.txt file ")

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

<br>

## clearTestLog

For internal use of the Marmoset Team. 😊

<!-- If the console is full of messages, or if you find confusing to read some message out of the whole thing, this is the best way to clean it.

```python
import mset

def RunPlugin():
    mset.clearTestLog ("\nThis message will appear in the log.txt file ")

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
``` -->

<br>