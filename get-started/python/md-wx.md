# WX Python Module

> Created by Fisher at 22:49 on 2016-10-15.

---



---

## Simple Window

```python
import wx      
app = wx.App()
frame = wx.Frame(None, -1, 'win.py')
frame.SetDimensions(0,0,640,480)


def onButton(event):
    print "Button pressed."

# Simple button
panel = wx.Panel(frame, wx.ID_ANY)
button = wx.Button(panel, wx.ID_ANY, 'Test', (10, 10))

# Image button.
bmp = wx.Bitmap("call-start.png", wx.BITMAP_TYPE_ANY)
button = wx.BitmapButton(panel, id=wx.ID_ANY, bitmap=bmp, size=(bmp.GetWidth()+10, bmp.GetHeight()+10))
# Button event.
button.Bind(wx.EVT_BUTTON, onButton)


# Information dialog.
wx.MessageBox('Pythonspot wxWidgets demo', 'Info', wx.OK | wx.ICON_INFORMATION)
# simple dialog
wx.MessageBox('A dialog', 'Title', wx.OK)
# warning dialog
wx.MessageBox('Operation could not be completed', 'Warning', wx.OK | wx.ICON_WARNING)
# error dialog
wx.MessageBox('Operation could not be completed', 'Error', wx.OK | wx.ICON_ERROR)
# Question dialog.
dlg = wx.MessageDialog(None, "Do you want to update?",'Updater',wx.YES_NO | wx.ICON_QUESTION)
result = dlg.ShowModal()
if result == wx.ID_YES:
    print "Yes pressed"
else:
    print "No pressed"
# File chooser dialog.
# Create open file dialog
# The definition of this method is: (parent, message, defaultDir, defaultFile, wildcard, style, pos)
openFileDialog = wx.FileDialog(frame, "Open", "", "",
                                      "Python files (*.py)|*.py",
                                       wx.FD_OPEN | wx.FD_FILE_MUST_EXIST)
openFileDialog.ShowModal()
print(openFileDialog.GetPath())
openFileDialog.Destroy()
# Input dialog.
dlg = wx.TextEntryDialog(frame, 'Enter some text','Text Entry')
dlg.SetValue("Default")
if dlg.ShowModal() == wx.ID_OK:
    print('You entered: %s\n' % dlg.GetValue())
dlg.Destroy()



# Menu
# Setting up the menu.
filemenu= wx.Menu()
filemenu.Append(101, "Open", "Open")
filemenu.Append(102, "Save", "Save")
filemenu.Append(wx.ID_ABOUT, "About","About")
filemenu.Append(wx.ID_EXIT,"Exit","Close")

# Creating the menubar.
menuBar = wx.MenuBar()
menuBar.Append(filemenu,"File") # Adding the "filemenu" to the MenuBar
frame.SetMenuBar(menuBar)  # Adding the MenuBar to the Frame content.

# Tabs
# @Ref: https://pythonspot.com/en/wxpython-tabs/



frame.Show()
# To put the window in the center of the screen call:
frame.Centre()

app.MainLoop()
```

---

















---
