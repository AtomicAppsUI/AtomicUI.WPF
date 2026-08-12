# AtomicUI.WPF

Modern WPF theme for .NET Framework and modern .NET.  
Premium Fluent-inspired UI for native WPF desktop applications.

**Modern UI. Minimal XAML. 2026-ready. Atomic speed.**

Move beyond the default Windows 11 look.  
**AtomicUI.WPF** is a modern evolution of Fluent design — a tactile, high-end visual language built for polished WPF desktop applications.

**Beyond flat:** Glass-morphism, refractive depth, layered surfaces, and smooth motion give your app a "future Windows" feel without switching frameworks.

**Zero Learning Curve:** AtomicUI styles native WPF controls automatically. No `Atomic:Button`, no `ui:Button`, no `EditButton` — it's just a normal `Button`. No custom markup, no redesigning your UI, no wrestling with massive XAML templates just to change a color. Keep your existing XAML — it just looks modern.

**Better than Microsoft's defaults:** We've taken Fluent, polished it,
deepened it, and turned it into a premium professional design system
that outclasses the .NET 10 themes.

**Legacy power:** Bring a 2026‑grade UI to apps running on .NET
Framework 4.5.1+. No migration to .NET 10, WinUI, or MAUI required.

## 🚀 Try the Official AtomicUI Gallery

Explore AtomicUI.WPF in a real desktop application with live controls,
animations, themes, layouts, and modern WPF styling examples.

📦 Microsoft Store:
https://apps.microsoft.com/detail/9PHND2W8WGG7?hl=en-us&gl=GB&ocid=pdpshare

The gallery demonstrates:
- Modern Buttons, TextBoxes, ComboBoxes, DataGrids, Tabs, Menus, and more
- Light & Dark themes
- Smooth animations and transitions
- Modernized WPF layouts and surfaces
- Native WPF controls styled with AtomicUI

<img width="500"  alt="Dashboard" src="https://raw.githubusercontent.com/AtomicAppsUI/AtomicUI.WPF/main/docs/images/Dashboard.png" />
<img width="500"  alt="BasicInput" src="https://github.com/user-attachments/assets/62d03c31-caf1-4d5c-97a5-7440b8e0ece2" />

<img width="500"  alt="Text" src="https://github.com/user-attachments/assets/8d03a581-d7ad-4b2e-ae7e-f5d44720e0ed" />
<img width="500"  alt="DateAndCalendar" src="https://github.com/user-attachments/assets/96c6b6ed-871b-476d-8535-8d052a75a18d" />

<img width="500"  alt="Collections" src="https://github.com/user-attachments/assets/8be587f4-e927-4623-90f2-16a06d16d658" />
<img width="500"  alt="WorkspaceDemo" src="https://github.com/user-attachments/assets/76c631df-d323-4edb-92a2-497aa8551578" />
<img width="500"  alt="WorkspaceDemo22" src="https://github.com/user-attachments/assets/00b06a30-9ef4-42a3-8245-9d65bc388b10" />

------------------------------------------------------------------------

## 🖥️ Built with AtomicUI

A couple of commercial products using AtomicUI.WPF:

### Map Secrets

**Interactive Map Maker -- Turn Any Image Into a Custom Map** is a
desktop mapping application built with WPF and AtomicUI.

<img width="500" alt="trails2" src="https://github.com/user-attachments/assets/cdfe53d0-d4f9-4621-8d4f-788e8a876c58" />
<img width="500"  alt="event4" src="https://github.com/user-attachments/assets/8d87ab91-6b2d-41e7-b3bf-e9c477a4198d" />

<table>
  <tr>
    <td valign="center">
      <img width="500" src="https://github.com/user-attachments/assets/03045f06-c9e1-4ecc-9302-1d3bb94eb4b3" />
    </td>
    <td valign="top">
      <img width="300" src="https://github.com/user-attachments/assets/ff0ad5d4-a55b-4f1d-99c6-5d8127a8bb46" />
    </td>
  </tr>
</table>


### Tank Secrets

**Tank Secrets** is a Windows aquarium management application built with
WPF and AtomicUI.

<img width="500" alt="Map Secrets - Dashboard" src="https://github.com/user-attachments/assets/e631b4d3-e4e0-4985-ba42-2d469ae0de45" />

<img width="500" alt="Tank Secrets - Water Parameters" src="https://github.com/user-attachments/assets/7ed7470a-3861-4a42-97a6-95dfcb514f94" />

Both applications use native WPF controls styled with AtomicUI.

------------------------------------------------------------------------

## ✨ Features

-   Modern Windows 11-style rounded edges and fluent animations\
-   Dark & Light themes included\
-   Custom window chrome with smooth transitions\
-   Drop-in integration with minimal XAML changes\
-   Backward compatible: .NET Framework 4.5.1+ and modern .NET, Windows
    7 → 11

------------------------------------------------------------------------

## 🧱 Styled WPF Controls

These controls are styled using pure XAML and integrate seamlessly:

-   Button / ToggleButton\
-   CheckBox / RadioButton\
-   ComboBox / ListBox\
-   Expander\
-   ProgressBar\
-   Slider\
-   TextBlock / TextBox

------------------------------------------------------------------------

## 🧪 Custom Controls

-   `ModernWindow` with custom chrome\
-   Custom Calendar\
-   Custom DatePicker\
-   Loading Animation

------------------------------------------------------------------------

## 🧩 Compatibility

-   **.NET Framework:** 4.5.1 and later (tested on 4.5.1, 4.6.2, 4.8)\
-   **.NET (Core/Modern):** 6, 7, 8, 9, 10 (Windows only)\
-   **OS:** Windows 7 → Windows 11

------------------------------------------------------------------------

## 🚀 Getting Started

### 1. Install AtomicUI.WPF

``` powershell
dotnet add package AtomicUI.Wpf
```

### 2. Add AtomicUI resources

#### Using `ModernWindow`

If your application uses `ModernWindow`, **do not add `DarkTheme.xaml` or `LightTheme.xaml`**.

You only need to merge `Generic.xaml`:

```xml
<ResourceDictionary>
  <ResourceDictionary.MergedDictionaries>
    <ResourceDictionary Source="/AtomicUI;component/Themes/Generic.xaml" />
  </ResourceDictionary.MergedDictionaries>
</ResourceDictionary>
```

`ModernWindow` automatically loads and manages the active Dark or Light theme.

> **Important:** When using `ModernWindow`, reference `Generic.xaml` only. Do not manually merge a theme dictionary.

##### Theme selection

Set the theme directly on `ModernWindow` using `IsDarkTheme`:

```xml
<ui:ModernWindow
    ...
    IsDarkTheme="True">
</ui:ModernWindow>
```

- `IsDarkTheme="True"` — Dark theme
- `IsDarkTheme="False"` — Light theme (default)

##### Built-in theme toggle

`ModernWindow` includes a built-in theme toggle button that allows users to switch between Dark and Light themes.

The button is shown by default. You can control its visibility with `ShowThemeToggleButton`:

```xml
<ui:ModernWindow
    ...
    IsDarkTheme="True"
    ShowThemeToggleButton="True">
</ui:ModernWindow>
```

To hide the theme toggle:

```xml
<ui:ModernWindow
    ...
    ShowThemeToggleButton="False">
</ui:ModernWindow>
```

This lets you either provide theme switching directly from the `ModernWindow` title bar or control the application's theme yourself.


#### Using a standard WPF `Window`

If you are **not** using `ModernWindow`, merge `Generic.xaml` together
with the theme you want to use.

**Dark theme**

``` xml
<ResourceDictionary>
  <ResourceDictionary.MergedDictionaries>
    <ResourceDictionary Source="/AtomicUI;component/Themes/DarkTheme.xaml" />
    <ResourceDictionary Source="/AtomicUI;component/Themes/Generic.xaml" />
  </ResourceDictionary.MergedDictionaries>
</ResourceDictionary>
```

**Light theme**

``` xml
<ResourceDictionary>
  <ResourceDictionary.MergedDictionaries>
    <ResourceDictionary Source="/AtomicUI;component/Themes/LightTheme.xaml" />
    <ResourceDictionary Source="/AtomicUI;component/Themes/Generic.xaml" />
  </ResourceDictionary.MergedDictionaries>
</ResourceDictionary>
```

### 3. Use `ModernWindow` (optional)

Replace your WPF window with `ModernWindow` if you want AtomicUI's
custom window chrome and automatic theme handling:

``` xml
<ui:ModernWindow
    x:Class="MyApp.MainWindow"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:ui="clr-namespace:AtomicUI.CustomControls;assembly=AtomicUI"
    Title="My App">
  <!-- Your content -->
</ui:ModernWindow>
```

``` csharp
public partial class MainWindow : ModernWindow
{
    public MainWindow()
    {
        InitializeComponent();
    }
}
```

### 4. Add a license key when required

``` csharp
using AtomicUI;

public partial class App : Application
{
    protected override void OnStartup(StartupEventArgs e)
    {
        ThemeManager.SetKey("MY-LICENSE-KEY");
        base.OnStartup(e);
    }
}
```

A license key is only required for paid licenses.

That's it --- your existing native WPF controls can now use AtomicUI
styling.

## 📬 Support

Need help with setup, licensing, or integration?

-   Discord: https://discord.gg/5QN4qyGP
-   Email: dan@atomicapps.dev

## ⚡ Advanced Scenarios (Still Super Easy)

1.  Keeping Theme Styling When Overriding Control Styles AtomicUI
    automatically styles all native WPF controls. But if you create your
    own custom style without a BasedOn, you replace the entire style ---
    which means the theme can't apply its visuals.

❌ What not to do This overrides the entire TextBox style, removing
AtomicUI's styling:

``` xml

<TextBox Height="40" AcceptsReturn="True" Text="{Binding Notes}">
    <TextBox.Style>
        <Style TargetType="{x:Type TextBox}">
            <Setter Property="FontSize" Value="30" />
        </Style>
    </TextBox.Style>
</TextBox>
```

✅ Correct way (inherits AtomicUI's styling) To keep the theme's
visuals, base your style on the default TextBox style:

``` xml
<TextBox Height="40" AcceptsReturn="True" Text="{Binding Notes}">
    <TextBox.Style>
        <Style BasedOn="{StaticResource {x:Type TextBox}}" 
               TargetType="{x:Type TextBox}">
            <Setter Property="FontSize" Value="30" />
        </Style>
    </TextBox.Style>
</TextBox>
```

✔ Applies to all controls This rule applies to any control you
restyle: - Button - TextBox - ComboBox - ListBox - Slider - CheckBox -
Your own custom controls If you want to keep AtomicUI's visuals, always
use:

``` xml
BasedOn="{StaticResource {x:Type ControlName}}"
```

(This is standard WPF --- not an AtomicUI limitation) When you apply
your own style to a control, WPF replaces the entire style unless you
explicitly inherit from the existing one. This is normal WPF behavior,
and it applies to every theme library, including AtomicUI.

### 2. Style Not Found in Some Framework-Loaded Views

In some advanced scenarios, especially when a view is loaded dynamically
by Prism or another framework, WPF may try to resolve a `BasedOn` style
before the relevant AtomicUI style dictionary has been loaded for that
view.

This usually only matters when you override a control style like this:

``` xml
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

-   A Prism region dynamically loads a view
-   A module loads its own ResourceDictionaries separately
-   A dialog/window is created outside the main application visual tree
-   A custom control library has isolated resources
-   A `BasedOn` style is resolved before AtomicUI's global dictionaries
    finish loading

> Dark & Light themes are included. Accent color customization is
> planned.

------------------------------------------------------------------------

## 🎨 Theming

-   Dark and Light themes included (`Themes/DarkTheme.xaml`,
    `Themes/LightTheme.xaml`)
-   **Using `ModernWindow`: merge `Generic.xaml` only --- do not
    manually add `DarkTheme.xaml` or `LightTheme.xaml`**
-   `ModernWindow` automatically loads and manages the active theme
-   Using a standard WPF `Window`: merge `Generic.xaml` together with
    the theme you want to use
-   Use `DynamicResource` where your own resources need to react to
    theme changes
-   Accent color customization is planned for a future release

------------------------------------------------------------------------

## 📄 Licensing

AtomicUI.WPF uses a perpetual licensing model.

### Personal & Indie --- Free

Free with no time limit for:

-   Personal and hobby projects
-   Independent developers
-   Commercial applications you develop and distribute independently

No guaranteed support is included.

### Commercial Licenses

Paid licenses are available for:

-   Individual developers working for an organisation, employer, or
    client
-   Development teams
-   Enterprise organisations

Commercial licenses are perpetual and include updates and support for
the included support period.

See [Pricing](https://atomicapps.dev/pricing) for current plans,
pricing, and full licensing details.

AtomicUI.WPF is distributed as a compiled-only NuGet package (no
source).

------------------------------------------------------------------------

## 🧠 FAQ

**Q: Can I use AtomicUI in a commercial app?**\
A: Yes. Independent developers can use the free Personal & Indie license
for applications they develop and distribute independently. A paid
license is required for employer, client, team, or other organisational
commercial use.

**Q: Is the source code included?**\
A: No. AtomicUI.WPF is distributed as a compiled-only package.

**Q: Do I need to replace standard WPF controls?**\
A: No. AtomicUI styles native WPF controls, so you can keep using normal
controls such as `Button`, `TextBox`, `ComboBox`, and `ListBox`.

**Q: Do I need to merge a theme dictionary when using ModernWindow?**\
A: No. Merge `Generic.xaml` only. `ModernWindow` automatically handles
the active Dark or Light theme, so do not manually add `DarkTheme.xaml`
or `LightTheme.xaml`.

------------------------------------------------------------------------

## 📦 Roadmap

✅ **AtomicUI Gallery available in the Microsoft Store**

1. ✅ Expanded sample application
2. ✅ Modern TreeView enhancements
3. ✅ .NET 10 support
4. .NET 11 support
5. ✅ Light theme refinement and polish
6. Accent color customization support
7. ✅ Validation styling improvements
8. Layout density support (Compact / Comfortable)
9. Comprehensive theming documentation and guides
10. AtomicUI.WinUI - Preview
11. AtomicUI.Avalonia - Preview

------------------------------------------------------------------------

## 🌐 Links

-   Website: [atomicapps.dev](https://atomicapps.dev)
-   Demo: [atomicapps.dev](https://atomicapps.dev/demo)
-   Pricing: [atomicapps.dev/pricing](https://atomicapps.dev/pricing)\
-   YouTube:
    [AtomicAppsOfficial](https://www.youtube.com/@AtomicAppsOfficial)\
-   X (Twitter): [@AtomicAppsUI](https://x.com/AtomicAppsUI)
