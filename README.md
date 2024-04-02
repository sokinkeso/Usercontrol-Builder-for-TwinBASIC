# Usercontrol Builder for TwinBASIC

Back in 90's when I was doing my first steps with vb6, ActiveX Control Interface Wizard was my favorite addin .
Thanks to the new Add-in subsystem of TwinBasic, I started creating my "Usercontrol Builder" addin.

*** Usercontrol Builder addin for TwinBasic ***
*** --------------------------------------- ***
Features:

- Wizard includes 6 pages (steps)
  - Page_1: Select one of the available usercontrols in your project. You can use the filters above the list for finding the desired members (if no usercontrols exist, the wizard will not open)
  - Page_2: Select from the list on the left, the built-in members that you want to include in your UC.
  - Page_3: Create your custom members. Write the name of the member in the text box, select its type and press [Add Member]. You can also edit or delete any of your custom members.
  - Page_4: Map any of the selected members (built-in or custom) with members of included controls in the Usercontrol.
  - Page_5: Fill in any extra info for the unmapped members.
  - Page_6: Pressing [Finish], the generated code will be inserted in the UC's codeEditor, at the top lines. You can see a summary or the generated code (and copy it to the clipboard), before pressing the [Finish].
 
- About mapping:
	- if you map a built-in member with the same member of a control, your UC will use the implementation of the included control.
	- if you map a custom member, with an existing member of a control, your UC will use the implementation of the included control but will be exposed with a different name (the name of the custom member)
	- if you map a built-in member with a different member on a control, the implementation of the control's member will be used. In this case the wizard will also generate a warning, to avoid wrong mapping.

*** New features compared to VB6: 
- Continuous mapping. Holding down the Ctrl key, you can map members to the last successful mapped control.
- Settings page
- UserControl Builder, includes tB's new data types (LongLong, LongPtr, Decimal)

- You can press the [Finish] button at any page of the wizard. (included in Settings)

- Supported controls for mapping (until now):
Usercontrol, Checkbox, ComboBox, CommandButton, DirList, DriveList, FileList, Frame, HScrollBar, Image, Label, Line, ListBox, OptionButton, PictureBox, Shape, TextBox, VScrollBar

- Important note: The Builder does not read (for now) any pre-existing code. It works one way (only generating code, not replacing)

- There are some known issues (like tabIndex) that will be solved in the future.

**Status (Nov 11th):** 

**Update (August 10th):** 

**Update (August 7th): Beta 2 Released!** 

