<div align="center">

## A very COOL color pick dialog with a color dropper like Photoshop and Frontpage XP


</div>

### Description

A very COOL color pick dialog with a color dropper like Photoshop and Frontpage XP
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[ucancode](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/ucancode.md)
**Level**          |Advanced
**User Rating**    |3.7 (11 globes from 3 users)
**Compatibility**  |Microsoft Visual C\+\+
**Category**       |[Controls/ Forms/ Dialogs/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-dialogs-menus__3-3.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/ucancode-a-very-cool-color-pick-dialog-with-a-color-dropper-like-photoshop-and-frontpage-x__3-3503/archive/master.zip)





### Source Code

<!--#include virtual="header.shtml" -->
<!--#include virtual="/global/getCss.inc" -->
<CENTER>
<p><b><font size="5">A very COOL color pick dialog with a color dropper like Photoshop and Frontpage
XP</font></b></p>
</CENTER><HR>
<!-- Author and contact details -->
<p>This article was contributed by
<a href="mailto:jack@ucancode.com">Jack Misic</a> </p>
<!-- For which environment is this code specific??? -->
<p><u>Environment:</u> Visual C++
<p><i>A very COOL color pick dialog with a color dropper like Photoshop and Frontpage
XP</i></p>
<h2>Introduction</h2>
<p><b>File reference:</b></p>
   <p class="MsoNormal"><span lang="EN-US">Prebuild version:
   <b>ColorPicker16_exe.zip</b> <b>120 KB </b>(A dialog for choosing colors)</p>
<p class="MsoNormal">Class Ref: <b>
ColorPickerClass.chm</b> <b>119KB </b>(Build by UCanCode DocVizor)</p>
<p class="MsoNormal">Source Code:<b>ColorPicker16_src.zip
65KB </b>(Build with MS Visual C++ 6.0)</p>
</span>
<p><i>First three are in demo project file below. Source code available below too.</i></p>
<p><b>The key features are as follows:</b></p>
<ol>
<li>ColorPicker provides a default color panel, which includes over 144 frequent colors.</li>
<li>ColorPicker provides a custom button for opening Windows Common Color Select Dialog. You can select more color here.</li>
<li>ColorPicker provides the color contrast between current selection and new selection.</li>
<li>ColorPicker provides a select button
<img border="0" src="ColorPicker01.gif" width="114" height="21">, when you hold the left button of mouse on select button, the cursor has become to a color dropper<img border="0" src="ColorPicker02.gif" width="25" height="21"> like Photoshop and Frontpage 2000. You can get any color on the screen via this dropper.</li>
<li>ColorPicker shows both the RGB value and Hex Value of the current selection color./li>
<li>The color panel will load new palette as soon as the system color range has been changed.</li>
<li>ColorDropper provides 6 color panels for choosing. You can change it during run time.</li>
<li>The most important thing is that, we provide the
full source code (100% MFC), ~{!-~}.</li>
<li><span lang="EN-US">
   <b><font color="#ff0000">(New)</font></b>Full
   keyboard support.</span></li>
</ol>
<p><b>Screen Shot:</b></p>
   <p class="MsoNormal"><img border="0" src="ColorPicker05.gif" width="312" height="257"></p>
   <p class="MsoNormal"><b>(Screen 1)</b></p>
   <p class="MsoNormal"><img border="0" src="ColorPicker03.gif" width="202" height="173"></p>
   <p class="MsoNormal"><b>(Screen 2)</b></p>
<p><img border="0" src="ColorPicker04.jpg" width="553" height="355"></p>
<p><b>(Screen 3)</b></p>
   <p class="MsoNormal"><b><span lang="EN-US">
   How to use it:</span></b></p>
   <p class="MsoNormal"><b><span lang="EN-US">&nbsp;</span></b><span lang="EN-US">The
   steps for usage are as follows:</span></p>
   <p class="MsoNormal"><span lang="EN-US"><b>
   1.</b>Add code in those head files
   where you want to display Color Picker Dialog.</span></p>
   <p class="MsoNormal">
   #include &quot;FODropColorButton.h&quot;</p>
   <p class="MsoNormal">
   enum { IDD = IDD_DIALOG_COLORPICKER };<br>
   CFODropColorButton m_wndColor3;<br>
     </font>CFODropColorButton m_wndColor2;<br>
   CFODropColorButton m_wndColor1;<br>
   CFOHyperLink m_newVersion;<br>
   //}}AFX_DATA</p>
   <p class="MsoNormal"><span lang="EN-US"><b>
   2.</b>Add code in those files/events
   when you need to get color value.</span></p>
   <p class="MsoNormal">CDialog::DoDataExchange(pDX);<br>
     //{{AFX_DATA_MAP(CNewPickerDlg)<br>
     DDX_Control(pDX, IDC_FO_TEST_BUTTON3, m_wndColor3);<br>
     DDX_Control(pDX, IDC_FO_TEST_BUTTON2, m_wndColor2);<br>
     DDX_Control(pDX, IDC_FO_TEST_BUTTON1, m_wndColor1);<br>
     //}}AFX_DATA_MAP<br>
     DDX_FODropColorButton(pDX,IDC_FO_TEST_BUTTON1,crColor1);<br>
     DDX_FODropColorButton(pDX,IDC_FO_TEST_BUTTON2,crColor2);<br>
     DDX_FODropColorButton(pDX,IDC_FO_TEST_BUTTON3,crColor3);</p>
<p>Everything is OK! </p>
<p><b>Technical Details </b></font></p>
   <p class="MsoNormal"><span lang="EN-US">Color
   Picker Dialog is constructed with classes as follows;</span></p>
   <p class="MsoNormal"><span lang="EN-US">
   <b>1.CFOColorButton</b> File
   Reference</span>~{#:~}<span lang="EN-US">FOColorButton.h,
   FOColorButton.cpp</span></p>
   <p class="MsoNormal"><span lang="EN-US">
   <b>2.CFOColorCellObj</b> File
   Reference</span>~{#:~}<span lang="EN-US">FOColorCellObj.h,
   FOColorCellObj.cpp</span></p>
   <p class="MsoNormal"><span lang="EN-US">
   <b>3.CFOColorDialogObj</b>
   File Reference</span>~{#:~}<font face="Verdana"><font face="Tahoma"><span lang="EN-US">FOColorDialog.h,
   FOColorDialog.cpp</span></p>
   <p class="MsoNormal"><span lang="EN-US">
   <b>4.CFOColorPaletteControl</b>
   File Reference</span>~{#:~}<span lang="EN-US">FOColorPaletteControl.h,
   FOColorPaletteControl.cpp</span></p>
   <p class="MsoNormal"><span lang="EN-US">
   <b>5.CFODropPaletteWnd</b>File
   Reference</span>~{#:~}FODropPaletteWnd<span lang="EN-US">.h,
   FODropPaletteWnd.cpp</span></p>
   <p class="MsoNormal">
   <b>6<span lang="EN-US">.CFODropColorButton</span></b> <span lang="EN-US">
   File Reference</span>~{#:~}FODropColorButton<span lang="EN-US">.h,
   FODropColorButton.cpp</span></p>
   </font>
   <p class="MsoNormal"><b>7<span lang="EN-US">.CFODropColorPaletteControl</span> </b><span lang="EN-US">
   File Reference</span>~{#:~}FODropColorPaletteControl<span lang="EN-US">.h,
   FODropColorPaletteControl.cpp</span></p>
   <p class="MsoNormal"><b>8<span lang="EN-US">.CFODropColorPaletteWnd</span> </b><span lang="EN-US">
   File Reference</span>~{#:~}FODropColorPaletteWnd<span lang="EN-US">.h,
   FODropColorPaletteWnd.cpp</span></p>
   <p class="MsoNormal"><b>9</b><span lang="EN-US"><b>.CFOPopupColorPaletteWnd</b>File
   Reference</span>~{#:~}FOPopupColorPaletteWnd<span lang="EN-US">.h,
   FOPopupColorPaletteWnd.cpp</span></p>
   </font>
<p>All of the class inheritance diagrams are as follows:
</p>
   <p class="MsoNormal"><b>CWnd</b></p>
   <p class="MsoNormal"><span lang="EN-US">
   <xml>
   <o:OLEObject Type="Embed" ProgID="Photoshop.Image.6" ShapeID="_x0000_i1028" DrawAspect="Content" ObjectID="_1071558310">
   <o:WordFieldCodes>\s</o:WordFieldCodes>
   </o:OLEObject>
   </xml><img border="0" src="ColorPickerCWnd.gif" width="286" height="157"></span></p>
   <p class="MsoNormal"><b>CObject</b></p>
   <p class="MsoNormal"><span lang="EN-US">
   <img border="0" src="ColorPickercobject.gif" width="276" height="140"><xml>
   <o:OLEObject Type="Embed" ProgID="Photoshop.Image.6" ShapeID="_x0000_i1029" DrawAspect="Content" ObjectID="_1071558311">
   <o:WordFieldCodes>\s</o:WordFieldCodes>
   </o:OLEObject>
   </xml></span></p>
   <p class="MsoNormal"><b>CStatic</b></p>
   <p><img border="0" src="ColorPickerCStatic.gif" width="289" height="124"></p>
   <p><span style="font-weight: 700">
   CButton</span></p>
   <p>
   <span lang="EN-US">
   <xml>
   <o:OLEObject Type="Embed" ProgID="Photoshop.Image.6" ShapeID="_x0000_i1030" DrawAspect="Content" ObjectID="_1071558312">
   <o:WordFieldCodes>\s</o:WordFieldCodes>
   </o:OLEObject>
   </xml><img border="0" src="ColorPickerCButton.gif" width="270" height="120"></span></p>
   <p><span style="font-weight: 700">
   CDialog</span></p>
   <p><img border="0" src="ColorPickerCDialog.gif" width="278" height="74"></p>
<p>Click <b><a href="http://www.ucancode.net/" target="new">here</a></b> to view Our online profile and report bugs.</p>
<span style="FONT-WEIGHT: 700; " lang="EN-US">
<p></span><b>
<span style="FONT-WEIGHT: 700; " lang="EN-US">
Update V1.6<font color="#ff0000">(New!)</font></span></b><span style="FONT-WEIGHT: 700; " lang="EN-US"></p>
<ul type="square">
 <li>Add full keyboard supprt,you can use<b> left
 arrow</b>,<b>right arrow</b>,<b>up arrow</b>,<b>down arrow</b> and <b>tab</b>
 key to select color.</span><span style="FONT-WEIGHT: 700; " lang="EN-US"> </li>
</span>
<span style="FONT-WEIGHT: 700; " lang="EN-US">
 <li>Fixed a few bugs.<span style="FONT-WEIGHT: 700; " lang="EN-US"> </li>
</ul>
</span>
</span>
   <p><b>Update V1.5</b></p>
<ul type="square">
 <li>Add color palette support for color dialog.</li>
 <li>Add a cool drop color picker button.</li>
 <li>Fixed a few bugs.</li>
</ul>
   <p><b>Update V1.2</b></p>
<ul type="square">
 <li>Add a specify image static class.</li>
 <li>Add support 3D color table.</li>
 <li>Fixed a few bugs.</li>
</ul>
<h3>Downloads</h3>
<a href="ColorPicker16_exe.zip">Download demo project -
213 Kb</a><br>
<a href="ColorPicker16_src.zip">Download source - 64 Kb</a><br>
</font>
<h3>History</h3>
Date Posted: March 13, 2002
Date Last Updated (V1.6)<BR>
<!--comments-->
</font>
<ul>
<!--startlist-->
</ul>
<!--#include virtual="footer.shtml" -->

