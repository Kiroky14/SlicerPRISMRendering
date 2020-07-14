# SlicerPRISMRendering

1. [ Introduction and Acknowledgements. ](#intro)
2. [ Module Description. ](#desc)
3. [ Use Cases. ](#usec)
4. [ Tutorials. ](#tutos)
5. [ Panels and their use. ](#panels)
6. [ Similar Modules. ](#similar)
7. [ References. ](#ref)
8. [ Information for Developers. ](#info)

	* [ Limitations. ](#lim)
	* [ Key nodes and classes. ](#key)
	* [ How Tos. ](#howto)

<a name="intro"></a>

## Introduction and Acknowledgements
**Title**: SlicerPRISM

**Author(s)/Contributor(s)**: Simon Drouin, Professor at École de technologie supérieure (ÉTS), Montréal, Tiphaine RICHARD, Student Intern at ÉTS.

**License**: slicer4

**Acknowledgements**: 

**Contact**: Tiphaine RICHARD, tiphainejh@gmail.com

<a name="desc"></a>

## Module Description
This module is an implementation of the PRISM customizable volume rendering framework in 3D Slicer. Slicer version 4.11.0 is needed for this module.

<a name="usec"></a>

## Use Cases

<a name="tutos"></a>

## Tutorials

<a name="rendering"></a>

### Rendering a volume

1. Open the "Data" section.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/render/1.png" width ="40%"/>
2. Select your volume in the comboBox.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/render/2.png" width ="40%"/>    
3. Open the "View Setup" section.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/render/3.png" width ="40%"/>
4. Apply the volume rendering to your volume by clicking on the "Volume Rendering" checkBox.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/render/4.png" width ="40%"/>

### Applying a shader to a volume

1. [Render the volume](#rendering).
2. Open the "Custom Shader" section.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/applyCS/2.png" width ="40%"/>
3. Select the shader of your choice in the comboBox.

4. Adjust the different parameters.

5. If you are currently developping the shader you can click on the "..." button in order to reload, duplicate or open the shader :
    
    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/applyCS/345.png" width ="40%"/>

    * Reload the shader by clicking on the "Reload" button. This will reload all the new functionnalities added to the file containing the shader.
    * Duplicate the shader by clicking on the "Duplicate" button. This will create a duplicate class of the class containing the shader.
    * Open the shader by clicking on the "Open" button. This will open the class containing the shader in your favorite editor.
    
    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/applyCS/6.png" width ="40%"/>

### Modifying the ROI of a volume

1. [Render the volume](#rendering).
2. Enable the cropping of the volume with the ROI by clicking on the "Enable Cropping" checkBox.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/modifyROI/2.png" width ="40%"/>    
3. Display the ROI of the volume by clicking on the "Display ROI" checkBox.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/modifyROI/3.png" width ="40%"/>
4. You can scale and rotate the ROI :

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/modifyROI/45.png" width ="40%"/>

    * Scale the ROI :
        1. Enable the scalling of the ROI by clicking on the "Enable Rotation" checkBox.
        2. Select one of the handle of the ROI and move it towards the center or the outside of the volume to scale the ROI.

        <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/modifyROI/scale.gif" width ="40%"/>    
    * Rotate the ROI :
        1. Enable the rotation of the ROI by clicking on the "Enable Rotation" checkBox.
        2. Select one of the side of the ROI and move it in any direction to rotate the ROI.

        <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/modifyROI/rotate.gif" width ="40%"/>

### Creating a new shader

1. Open the "Modify or Create Custom Shader" section.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/createCS/1.png" width ="40%"/>
2. In the comboBox, select "Create new Custom Shader".

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/createCS/2.png" width ="40%"/>
3. Type the name of the shader that will be used as a class name.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/createCS/3.png" width ="40%"/>
4. Type the display name of the shader that will be used in the UI.
5. Click the "Create" button.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/createCS/45.png" width ="40%"/>
6. You can either :
    * Click on the "Edit" button and modify the python class manually.
    * Use the [ Add Code ](#addcode) and [ Add Parameter ](#addparam) tabs to modify the python class with the UI : 

        <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/createCS/6.png" width ="40%"/>

### Modifying an existing shader

1. Open "Modify or Create Custom Shader" section.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/modifyCS/1.png" width ="40%"/>
2. In the comboBox, select the shader to modify.

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/modifyCS/2.png" width ="40%"/>
3. Use the [ Add Code ](#addcode) and [ Add Parameter ](#addparam) tabs to modify the python class UI : 

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/modifyCS/3.png" width ="40%"/>

<a name="addparam"></a>

### Adding a parameter to a shader from the UI

1. In the comboBox, select the type of the parameter to add to the shader. 

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/addParam/1.png" width ="40%"/>
2. Type the name of the parameter that will be used inside the shader.  

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/addParam/2.png" width ="40%"/>
3. Type the display name of the parameter that will be used in the UI.  

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/addParam/3.png" width ="40%"/>
4. Modify the values according to the parameter.  
5. Click the "Add Parameter" button.    

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/addParam/45.png" width ="40%"/>
6. Repeat steps 1-5 for each wanted parameter.

<a name="addcode"></a>

### Adding code to a shader from the UI

1. In the first comboBox, select the tag type of the code to be added to the shader.  

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/addCode/1.png" width ="40%"/>
2. In the second comboBox, select the tag of the code to be added to the shader.  

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/addCode/2.png" width ="40%"/>
3. To add the code you can either :  

    <img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/tutorials/addCode/3.png" width ="40%"/>   

    * Enter the code in the text area and click on the "Modify" button.
    * Click on the "Open File" button to enter the code directly in the python file.
4. Repeat steps 1-3 for each wanted code replacement.


<a name="panels"></a>

## Panels and their use

<table style="table-layout: fixed; width:100%; border: 1px grey; border-collapse: collapse;">
<tr>
<td style=" width:50%">
<ul><li><b>Data</b> : Contains the volume required for SlicerPRISM. </li>
<ul><li><b>Image Volume</b> : Select the current volume to render. </li></ul>
</ul>
</td>
<td>
<img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/Data.png" alt="Data" width ="100%" title="Data"/>
</td>
</tr>
<tr>
<td style="width:50%">
<ul> 
<li> <b>View Setup</b> : Contains the controls for rendering the volume as well as controls for the cropping box (ROI) of the volume. </li>
<ul>
<li><b>Volume Rendering</b> : Enable/Disable rendering the volume.</li>
<li><b>Enable Cropping</b> : Enable/Disable cropping the volume.</li>
<li><b>Display ROI</b> : Enable/Disable displaying the ROI of the volume.</li>
<li><b>Enable Scaling</b> : Enable/Disable scaling the ROI of the volume.</li>
<li><b>Enable Rotation</b> : Enable/Disable rotating the ROI of the volume.</li>
</ul>
</ul>
</td>
<td align="center" style="width:50%">
<img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/ViewSetup.png" alt="ViewSetup" width ="100%" title="ViewSetup"/>
</td>
</tr>
<tr>
<td style="width:50%">
<ul> 
<li><b>Custom Shader</b> : Controls of the shader.</li>
<ul>
<li><b>Custom Shader</b> : Name of the shader to be applied during the rendering.</li>
<li><b>Reload</b> : Reload the current shader.</li>
<li><b>Open</b> : Open the current shader source code.</li>
<li><b>Duplicate</b> : Duplicate the current shader source code.</li>
</ul>
</ul>
</td>
<td align="center" style="width:50%">
<img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/CustomShader.png" alt="CustomShader" width ="100%" title="CustomShader"/>
</td>
</tr>
<tr>
<td rowspan=3 style="width:50%">
<ul> 
<li><b>Modify or Create Custom Shader</b> : Create or Modify a custom shader and add parameters.</li>
<ul>
<li><b>Shader</b> : Name of the shader to modify or <i>Create new Custom Shader</i> to create a new one.</li>
<li><b>Class Name</b> : Name of the class that will be created.</li>
<li><b>Display Name</b> : Name of the shader that will be displayed in the UI.</li>
<li><b>Create</b> : Create the class.</li>
<li><b>Add Code</b> : Add a code that will replace a specific shader tag in the shader.</li>
<ul>
<li><b>Tag Type</b> : Type of the tag to be remplaced in the shader.</li>
<li><b>Shader Tag</b>: Tag to be remplaced in the shader.</li>
<li><b>Shader Code</b> : Code to replace the specified tag in the shader. Can be added directly in the </li>file by clicking <i>Open File</i>.
<li><b>Open File</b> : Open the class containing the shader.</li>
<li><b>Modify</b> : Apply the modifications the the class.</li>
</ul>
<li><b>Add Param</b> : Add specified parameters to the class that will be used in the shader.</li>
<ul>
<li><b>Type</b> : Type of the parameter.</li>
<li><b>Name</b> : Name of the parameter that will be used in the shader.</li>
<li><b>Display Name</b> : Name of the parameter that will be displayed in the UI.</li>
<li><b>Add Parameter</b> : Add the parameter in the class.</li>
</ul>
</ul>
</ul>
</td>
<td align="center" style="width:50%">
<img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/MCCustomShader.png" alt="MCCustomShader" width ="100%" title="MCCustomShader"/>
</td>
</tr>
<tr>
<td align="center" style="width:50%">
<img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/MCCustomShaderCode.png" alt="MCCustomShaderCode" width ="100%" title="MCCustomShaderCode"/>
</td>
</tr>
<tr>
<td align="center" style=" width:50%">
<img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/MCCustomShaderParam.png" alt="MCCustomShaderParam" width ="100%" title="MCCustomShaderParam"/>
</td>
</tr>
</table>

<p align="center"><img src="https://raw.githubusercontent.com/ETS-vis-interactive/SlicerPRISM/master/docs/source/images/UnderConstruction.gif" alt="UnderConstruction" width ="50%" title="MCCustomShaderParam"/></p>

<a name="similar"></a>

## Similar Modules

[VolumeRendering](https://www.slicer.org/wiki/Documentation/4.10/Modules/VolumeRendering)

<a name="ref"></a>

## References

[PRISM: An open source framework for the interactive design of GPU volume rendering shaders](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0193636)  

<a name="info"></a>

## Information for Developers

See [this page](https://ets-vis-interactive.github.io/SlicerPRISM/html/index.html) for the full documentation.

<a name="lim"></a>

### Limitations

<a name="key"></a>

### Key nodes and classes

<a name="howto"></a>

### How Tos