# Dialog

In case you don't know, Dialog is a very special window that lets you talk to the OS. You use it to open or save files.

In this case, windows are modal, and this only means they stop the flow of Toolbag until you are done negotiate with the OS.

<br>

## showOkCancelDialog

def showOkCancelDialog(title: str, prompt: str) ‑> bool

This command will open a modal dialog box. 'Title' will be the titlebar of the window and prompt the text inside the window.
Returns True or False depending on whether OK or Cancel is selected.

Useful when you want to confirm something with the user

```python
import mset

def RunPlugin():
    mset.showOkCancelDialog("Title of the window", "Message inside the box")

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```
<br>

## showOkDialog

def showOkDialog(title: str, prompt: str) ‑> bool

This command will open a modal dialog box. 'Title' will be the titlebar of the window and prompt the text inside the window.

The key difference with **showOkCancelDialog** is that **showOkDialog** always returns true no matter what.

Useful for sending a direct message to the user.

```python
import mset

def RunPlugin():
    mset.showOkDialog("Title of the window", "Message inside the box")

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

<br>

## showOpenFileDialog

def showOpenFileDialog(fileTypes: List[str] = [], multiple: bool = False) ‑> str

This command will open a modal dialog box so a file can be selected.

If a file is selected, showOpenFileDialog will return the full path.
If the cancel button is pressed, it will return and empty string.

Optionally, the fileTypes can be specified.


```python
import mset

def RunPlugin():

    result = mset.showOpenFileDialog("Title of the window", "Message inside the box")
    print(f"Dialog result: {result}")  # Debugging output

    if result:
        print(result)
    else:
        print("User closed the dialog without pressing OK")

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

<br>

## showOpenFolderDialog

def showOpenFolderDialog() ‑> str

This command will open a modal dialog box so a folder can be selected.

If a folder is selected, showOpenFileDialog will return the full path.
If the cancel button is pressed, it will return and empty string.

Yeah, it's the same as showOpenFileDialog but for folders.

```python
import mset

def RunPlugin():

    result = mset.showOpenFolderDialog()
    print(f"Dialog result: {result}")  # Debugging output

    if result:
        print(result)
    else:
        print("User closed the dialog without pressing OK")

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```

<br>

## showSaveFileDialog

def showSaveFileDialog(fileTypes: List[str] = []) ‑> str

This command will open a modal dialog box so a file can be save.

If a folder is selected, showOpenFileDialog will return the full path.
If the cancel button is pressed, it will return and empty string.


```python
import mset

def RunPlugin():

    result = mset.showSaveFileDialog()
    print(f"Dialog result: {result}")  # Debugging output

    if result:
        print(result)
    else:
        print("User closed the dialog without pressing OK")

window = mset.UIWindow("Test UI")
myButton = mset.UIButton("Run Plugin")
window.addElement(myButton)

myButton.onClick = RunPlugin
```


<br>