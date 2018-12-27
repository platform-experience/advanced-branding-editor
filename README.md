Advanced Branding Editor
==================
The Advanced Branding Editor application allows you to define branding options for custom portals, and configure them in a user friendly interface similar to that of the regular Branding Editor.

The regular Branding Editor allows configuration of the out-of-box Service Portal, however the hard-coded "bootstrap" styles defined in there for are severly limiting when applied to custom portals, or other Service Portal's offered by product lines such as Human Resources or Customer Service Management. Advanced Branding Editor offers greater flexibility in this regard - you can define as many variables as you want per portal, label them in a relevant way, and allow for simple configuration for any type of portal.

There are various other features and usability improvements over the out-of-box branding editor. Some examples are:

- Define a CSS selector per variable to offer a "Show me" functionality, highlighting where in the preview that the styling will affect.
- Reset a variable back to it's default state using the Reset button.
- Upload new images and replace them.
- Portal select dropdown allows filtering.

Screenshots
-------------------

<img src="screenshot.png">

<img src="abe.png">

Installaton
-------------------
1. Open Studio on your ServiceNow instance.
2. Click the **Import From Source Control** button.
3. As the value of the URL field use the following:
	`https://github.com/platform-experience/advanced-branding-editor.git`
4. Press the **Import** button

How it works
-------------------
The one prerequisite for the Advanced Branding Editor to work correctly is that your portal (and the widgets that make it up) have semantic and useable heirachy of SASS.

When loading the editor, the Branding Groups and Branding Variables tables will be scanned for relevant records to the selected portal. The SASS contained in the portal record will also be loaded, and the current value of each variable will be taken from it using a regular expression. Upon changing a variable's setting in the user interface, the value will be saved back into the SASS of the portal record again using a regular expression.

Usage
-------------------
The application comes with the branding groups and branding variables defined for the out-of-box Service Portal, however if you have any other portals then you will need to define groups and variables for these.
