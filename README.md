# FunctionGUI

FunctionGUI is a simple GUI library built using tkinter, designed to help you quickly create graphical user interfaces with ease.

## Installation

To install FunctionGUI, you can simply use pip:

```bash
pip install functiongui
```


# FunctionGUI

FunctionGUI is a simple GUI library built using tkinter, designed to help you quickly create graphical user interfaces with ease. 



## Usage
```python
import functiongui as fg

# Create the main window
root = fg.Window()

# Set the title
fg.Title(root, "FunctionGUI Example")

# Set design/theme
theme = fg.Design("cosmo")  # Uses ttkbootstrap

# Background Image
fg.BGImage(root, bg_image_path='your_image_path.jpg', width=500, height=400)

# BooleanVar for checkbox
check_var = fg.BulleanVar()

# Entry field
entry = fg.Entry(root, width=30, font="Helvetica", size=12, bg="white", fg="black", padx=5, pady=5)
fg.Place(entry)

# Button to print the entry value
def on_button_click():
    value = fg.GetEntry(entry)
    print("Entry value:", value)

button = fg.Button(root, text="Print Entry", command=on_button_click, font="Helvetica", size=12, bg="green", fg="white", width=20, height=2)
fg.Place(button, x=50, y=80)

# Label with StringVar
strvar = fg.StrVar(root, "Initial Text")
label = fg.Label(root, textvariabl=strvar, font="Arial", size=14, color="blue", wraplenght=200, width=30)
fg.Place(label)

# CheckBox
fg.ChexBox(root, text="Check me!", variable=check_var, command=lambda: print("Checkbox state:", check_var.get()))

# Dropdown
drop_var = fg.StrVar(root, "Option 1")
dropdown = fg.Dropdown(root, textvariable=drop_var, values=["Option 1", "Option 2", "Option 3"])
fg.Place(dropdown)

# Image display from file
fg.Image(root, "your_image_path.jpg", width=150, height=100)

# CSV functions (you can test separately)
fg.CVSWRITE("data.csv", [["Name", "Age"], ["Alice", 30]])
data = fg.CVSREAD("data.csv")
for row in data:
     print(row)

# File dialogs
open_path = fg.OpenFile("Choose a file")
save_path = fg.SaveFile("Save your file")

# Drag and Drop area
drag_and_drop = fg.DragDropArea(root)

# Scrollable widget demo
text_widget = tk.Text(root, height=5, width=40)
fg.ScrollBar(root, text_widget)
text_widget.pack()

# Exit & Close examples (uncomment if needed)
fg.Exit()

# close a window
fg.Close(root)

# Start the GUI loop
fg.Run(root)

```

## Bugs

If you are finding bugs in the code, please report them to me @aaroh.charne@gmail.com.
Please include a snippet of your code as well the problem. Thank You

## Please check out my other Library Calclab @https://pypi.org/project/Calclab/
```