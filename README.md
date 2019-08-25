
MaterialSkin+ for .NET WinForms
=====================

Theming .NET WinForms, C# or VB.Net, to Google's Material Design Principles **but open to customize**.
This is an open version of [Ignace Maes](https://github.com/IgnaceMaes) development called [MaterialSkin](https://github.com/IgnaceMaes/MaterialSkin)

<a href="https://www.youtube.com/watch?v=A8osVM_SXlg" target="_blank">![alt tag](http://i.imgur.com/JAttoOo.png)</a>

*High quality images can be found at the bottom of this page.*

---

#### Implementing MaterialSkin+ in your application

**1. Add the library to your project**

Clone this project from GitHub, compile the library and add it as a reference. We will upload as Nuget Package when the development is more advanced
  
**2. Add the MaterialSkin components to your ToolBox**

  Simply drag the MaterialSkin.dll file into your IDE's ToolBox and all the controls should be added there.
  
**3. Inherit from MaterialForm**

  Open the code behind your Form you wish to skin. Make it inherit from MaterialForm rather than Form. Don't forget to put the library in your imports, so it can find the MaterialForm class!
  
  C# (Form1.cs)
  ```cs
  public partial class Form1 : MaterialForm
  ```
  
  VB.NET (Form1.Designer.vb)
  ```vb
  Partial Class Form1
    Inherits MaterialSkin.Controls.MaterialForm
  ```
  
**4. Initialize your colorscheme**

  Set your preferred colors & theme. Also add the form to the manager so it keeps updated if the color scheme or theme changes later on.

**4.1. Use official Google's Material Design Principle colors**

C# (Form1.cs)
  ```cs
  public Form1()
  {
      InitializeComponent();

      var materialSkinManager = MaterialSkinManager.Instance;
      materialSkinManager.AddFormToManage(this);
      materialSkinManager.Theme = MaterialSkinManager.Themes.LIGHT;
      materialSkinManager.ColorScheme = new ColorScheme(Primary.BlueGrey800, Primary.BlueGrey900, Primary.BlueGrey500, Accent.LightBlue200, TextShade.WHITE);
  }
  ```

VB.NET (Form1.vb)
```vb
Imports MaterialSkin

Public Class Form1

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        Dim SkinManager As MaterialSkinManager = MaterialSkinManager.Instance
        SkinManager.AddFormToManage(Me)
        SkinManager.Theme = MaterialSkinManager.Themes.LIGHT
        SkinManager.ColorScheme = New ColorScheme(Primary.BlueGrey800, Primary.BlueGrey900, Primary.BlueGrey500, Accent.LightBlue200, TextShade.WHITE)
    End Sub
End Class
```
**4.2. Use custom color from String (non-official Google's Material Design Principle colors)**
If you want use a color palette that is not alloweb by Google's Material Design Principle, MaterialSkin+ supports custom colors only providing your colors Hex Codes to the wished ColorScheme parameter.

**Valid Parameter Formats**
| Parameter | Format |
| --- | --- |
| (#)ARGB | "#0000FF00" |
| (#)RGB | "#00FF00" |
| (#)ShortRGB | "#00F" |
| | |
| ARGB | "0000FF00" |
| RGB | "00FF00" |
| ShortRGB | "00F" |

Example:

C# (Form1.cs)
  ```cs
  public Form1()
  {
      InitializeComponent();

      var materialSkinManager = MaterialSkinManager.Instance;
      materialSkinManager.AddFormToManage(this);
      materialSkinManager.Theme = MaterialSkinManager.Themes.LIGHT;
      materialSkinManager.ColorScheme = new ColorScheme("#00480157", "#370142", "DC2EFF", "00BB5FCF", TextShade.WHITE);
  }
  ```

VB.NET (Form1.vb)
```vb
Imports MaterialSkin

Public Class Form1

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        Dim SkinManager As MaterialSkinManager = MaterialSkinManager.Instance
        SkinManager.AddFormToManage(Me)
        SkinManager.Theme = MaterialSkinManager.Themes.LIGHT
        SkinManager.ColorScheme = New ColorScheme("#00480157", "#370142", "DC2EFF", "00BB5FCF", TextShade.WHITE)
    End Sub
End Class
```
![alt-tag](https://i.imgur.com/66av3Gl.png)

**4.3. Use custom color from Decimal Integer (non-official Google's Material Design Principle colors)**
If you want use a color palette that is not alloweb by Google's Material Design Principle, MaterialSkin+ supports custom colors only providing your colors Hex Codes to the wished ColorScheme parameter.

**Valid Parameter Formats**
| Parameter | Format |
| --- | --- |
| ARGB | 0x0000FF00 |
| RGB | 0x00FF00 |
| ShortRGB | 0x00F |

Example:

C# (Form1.cs)
  ```cs
  public Form1()
  {
      InitializeComponent();

      var materialSkinManager = MaterialSkinManager.Instance;
      materialSkinManager.AddFormToManage(this);
      materialSkinManager.Theme = MaterialSkinManager.Themes.DARK;
      materialSkinManager.ColorScheme = new ColorScheme(0x00C926b3, 0xA1008B, 0xDC2EFF, 0x006E70FF, TextShade.WHITE);
  }
  ```

VB.NET (Form1.vb)
```vb
Imports MaterialSkin

Public Class Form1

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        Dim SkinManager As MaterialSkinManager = MaterialSkinManager.Instance
        SkinManager.AddFormToManage(Me)
        SkinManager.Theme = MaterialSkinManager.Themes.DARK
        SkinManager.ColorScheme = New ColorScheme(0x00C926b3, 0xA1008B, 0xDC2EFF, 0x006E70FF, TextShade.WHITE)
    End Sub
End Class
```
![alt-tag](https://i.imgur.com/SC2uoBJ.png)

---
#### State of the project

This project is under active development.

---

## Credits 👍
* **MaterialSkin for .NET WinForms:** [MaterialSkin for .NET WinForms](https://github.com/IgnaceMaes/MaterialSkin)

---

#### Contact

If you wish to contact me for anything you can get in touch at:

- Twitter: https://twitter.com/cygnus_project

---

#### Images

![alt tag](https://i.imgur.com/66av3Gl.png)

*A simple demo interface with MaterialSkin components.*

![alt tag](https://i.imgur.com/JV18LsX.png)

*The MaterialSkin checkboxes.*

![alt tag](https://i.imgur.com/gCRlDEZ.png)

*The MaterialSkin radiobuttons.*

![alt tag](https://i.imgur.com/NMwXRQS.png)

*The MaterialSkin ListView.*
