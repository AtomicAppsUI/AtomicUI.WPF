[README.md](https://github.com/user-attachments/files/22582030/README.md)
# AtomicUI.WPF

**Modern UI. Minimal XAML. 2026-ready. Atomic speed.**

Stop making apps that look like the Windows 11 Settings panel.
**AtomicUI.WPF** is the evolution of the Fluent design system — a tactile, high‑end visual language that Microsoft’s default themes simply can’t match.

**Beyond flat:** glass‑morphism, refractive depth, layered surfaces, and smooth motion that give your app a “future Windows” feel without switching frameworks.

**Zero Learning Curve:** Styles native WPF controls automatically.
No Atomic:Button, no ui:Button, no EditButton — it’s just a normal Button.
No custom markup, no redesigning your UI, no wrestling with massive XAML templates just to change a color. Keep your existing XAML — it just looks modern

**Better than Microsoft’s defaults:** We’ve taken Fluent, polished it, deepened it, and turned it into a premium professional design system that outclasses the .NET 10 themes.

**Legacy power:** Bring a 2026‑grade UI to apps running on .NET Framework 4.5.1+. No migration to .NET 10, WinUI, or MAUI required.

## 🚀 Try the Official AtomicUI Gallery

Explore AtomicUI.WPF in a real desktop application with live controls, animations, themes, layouts, and modern WPF styling examples.

📦 Microsoft Store:
https://apps.microsoft.com/detail/9PHND2W8WGG7?hl=en-us&gl=GB&ocid=pdpshare

The gallery demonstrates:
- Modern Buttons, TextBoxes, ComboBoxes, DataGrids, Tabs, Menus, and more
- Light & Dark themes
- Smooth animations and transitions
- Modernized WPF layouts and surfaces
- Real-world desktop UI examples built entirely with native WPF controls

<p align="left">
  <img src="https://github.com/user-attachments/assets/38db8b2a-01be-46f4-822f-81dadd4fe39d" width="250" />
  &nbsp;
  <img src="https://github.com/user-attachments/assets/e26e98df-637a-431e-9214-f34eab7284f4" width="250" />
</p>

<p align="left">
  <img src="https://github.com/user-attachments/assets/251e1736-ba79-456f-a0f2-ba0786745997" width="250" />
  &nbsp;
  <img src="https://github.com/user-attachments/assets/ad9fbe2c-057b-4a23-bdce-592d795f88ee" width="250" />
</p>

<p align="left">
  <img src="https://github.com/user-attachments/assets/1b26ba5f-7a98-48ad-83bd-8be195dbf2ec" width="250" />
  &nbsp;
  <img src="https://github.com/user-attachments/assets/702e582d-61cd-4023-aa77-3805cfdff1eb" width="250" />
</p>

<p align="left">
  <img src="https://github.com/user-attachments/assets/09a41a2e-3c93-413b-af42-ec94c8d90839" width="250" />
  &nbsp;
  <img src="https://github.com/user-attachments/assets/69bf2fae-a6eb-4609-9f1c-bef64586f3be" width="250" />
</p>


---

## ✨ Features

- Modern Windows 11-style rounded edges and fluent animations  
- Dark & Light themes included  
- Custom window chrome with smooth transitions  
- Drop-in integration with minimal XAML changes  
- Backward compatible: .NET 4.5.1 → .NET 9, Windows 7 → 11  

---

## 🧱 Styled WPF Controls

These controls are styled using pure XAML and integrate seamlessly:

- Button / ToggleButton  
- CheckBox / RadioButton  
- ComboBox / ListBox  
- Expander  
- ProgressBar  
- Slider  
- TextBlock / TextBox  

---

## 🧪 Custom Controls

- `ModernWindow` with custom chrome  
- Custom Calendar  
- Custom DatePicker  
- Loading Animation  

---

## 🧩 Compatibility

- **.NET Framework:** 4.5.1 and later (tested on 4.5.1, 4.6.2, 4.8)  
- **.NET (Core/Modern):** 6, 7, 8, 9 (Windows only)  
- **OS:** Windows 7 → Windows 11  

---

🚀 Getting Started

1. Install the NuGet package (coming soon):
   ```powershell
   dotnet add package AtomicUI.WPF
   ```

2. Merge the theme resource dictionary:
   ```xml
   <ResourceDictionary> 
     <ResourceDictionary.MergedDictionaries>
       <ResourceDictionary Source="pack://application:,,,/AtomicUI.WPF;component/Themes/DarkTheme.xaml" />
       <ResourceDictionary Source="pack://application:,,,/AtomicUI.WPF;component/Themes/LightTheme.xaml"/>
     </ResourceDictionary.MergedDictionaries>
   </ResourceDictionary>
   ```

3. Replace your main window with `ModernWindow`:
   ```xml
   <ui:ModernWindow
       x:Class="MyApp.MainWindow"
       xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
       xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
       xmlns:ui="clr-namespace:AtomicUI.CustomControls;assembly=AtomicUI"
       Title="My App">
     <!-- Your content -->
   </ui:ModernWindow>
   ```
   ```csharp
   public partial class MainWindow : ModernWindow
   {
       public MainWindow()
       {
           InitializeComponent();
       }
   }
   ```

4. The license key setup instructions
   ```csharp
    using AtomicUI;

    public partial class App : Application
    {
        //Only required for paid licenses
        protected override async void OnStartup(StartupEventArgs e)
        {
            ThemeManager.SetKey("MY-LICENSE-KEY");
            base.OnStartup(e);
        }
    }

   ```

That is all it takes, you are now running modern 2026 looking aplication.
Contact dan@atomicapps.dev for details.

⚡ Advanced Scenarios (Still Super Easy)

1. Keeping Theme Styling When Overriding Control Styles
AtomicUI automatically styles all native WPF controls.
But if you create your own custom style without a BasedOn, you replace the entire style — which means the theme can’t apply its visuals.

❌ What not to do
This overrides the entire TextBox style, removing AtomicUI’s styling:
```xml   

<TextBox Height="40" AcceptsReturn="True" Text="{Binding Notes}">
    <TextBox.Style>
        <Style TargetType="{x:Type TextBox}">
            <Setter Property="FontSize" Value="30" />
        </Style>
    </TextBox.Style>
</TextBox>
```

✅ Correct way (inherits AtomicUI’s styling)
To keep the theme’s visuals, base your style on the default TextBox style:

```xml
<TextBox Height="40" AcceptsReturn="True" Text="{Binding Notes}">
    <TextBox.Style>
        <Style BasedOn="{StaticResource {x:Type TextBox}}" 
               TargetType="{x:Type TextBox}">
            <Setter Property="FontSize" Value="30" />
        </Style>
    </TextBox.Style>
</TextBox>
```

✔ Applies to all controls
This rule applies to any control you restyle:
- Button
- TextBox
- ComboBox
- ListBox
- Slider
- CheckBox
- Your own custom controls
If you want to keep AtomicUI’s visuals, always use:

```xml
BasedOn="{StaticResource {x:Type ControlName}}"
```

(This is standard WPF — not an AtomicUI limitation)
When you apply your own style to a control, WPF replaces the entire style unless you explicitly inherit from the existing one. This is normal WPF behavior, and it applies to every theme library, including AtomicUI.

### 2. Style Not Found in Some Framework-Loaded Views

In some advanced scenarios, especially when a view is loaded dynamically by Prism or another framework, WPF may try to resolve a `BasedOn` style before the relevant AtomicUI style dictionary has been loaded for that view.

This usually only matters when you override a control style like this:

```xml
<Style BasedOn="{StaticResource {x:Type Label}}"
       TargetType="Label">
    <Setter Property="FontSize" Value="18" />
</Style>

<UserControl.Resources>
    <ResourceDictionary>
        <ResourceDictionary.MergedDictionaries>
            <ResourceDictionary Source="/AtomicUI;component/Themes/Styles/ModernLabelStyle.xaml" />
        </ResourceDictionary.MergedDictionaries>

        <Style BasedOn="{StaticResource {x:Type Label}}"
               TargetType="Label">
            <Setter Property="FontSize" Value="18" />
        </Style>
    </ResourceDictionary>
</UserControl.Resources>

/AtomicUI;component/Themes/Styles/ModernControlNameStyle.xaml

/AtomicUI;component/Themes/Styles/ModernButtonStyle.xaml
/AtomicUI;component/Themes/Styles/ModernTextBoxStyle.xaml
/AtomicUI;component/Themes/Styles/ModernComboBoxStyle.xaml
/AtomicUI;component/Themes/Styles/ModernLabelStyle.xaml
```

This is only needed in rare cases, typically when:

- A Prism region dynamically loads a view
- A module loads its own ResourceDictionaries separately
- A dialog/window is created outside the main application visual tree
- A custom control library has isolated resources
- A `BasedOn` style is resolved before AtomicUI’s global dictionaries finish loading

> Dark & Light themes are included. Accent color customization is planned.

---

## 🎨 Theming

- Dark & Light themes included (`Themes/Dark.xaml`, `Themes/Light.xaml`)  
- Use `DynamicResource` for color switching  
- Accent color customization planned for a future release  

---

## 📄 License

Commercial license required.  
A trial license activates automatically
Distributed as a compiled-only NuGet package (no source).  
See [Pricing](https://atomicapps.dev/pricing).  

---

## 🧠 FAQ

**Q: Can I use it in a commercial app?**  
A: Yes, but a paid license is required.  

**Q: Is the source code included?**  
A: No, this is a compiled-only package.  

**Q: Can I try it before buying?**  
A: A free demo NuGet and sample app will be available.  

---

## 📦 Roadmap

- .NET 10 support  
- Accent color customization  
- Light theme improvements  
- Sample/demo app  
- Theming guide & documentation  

---

## 🌐 Links

- Website: [atomicapps.dev](https://atomicapps.dev)
- Demo: [atomicapps.dev](https://atomicapps.dev/demo)
- Pricing: [atomicapps.dev/pricing](https://atomicapps.dev/pricing)  
- YouTube: [AtomicAppsOfficial](https://www.youtube.com/@AtomicAppsOfficial)  
- X (Twitter): [@AtomicAppsUI](https://x.com/AtomicAppsUI)  
