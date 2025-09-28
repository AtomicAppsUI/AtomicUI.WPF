[README.md](https://github.com/user-attachments/files/22582030/README.md)
# AtomicUI.WPF

**Modern UI. Minimal XAML. 2026-ready. Atomic speed.**

A modern WPF theme that brings Windows 11’s design language to any WPF app.  
Rounded edges, smooth animations, and polished Dark & Light themes — compatible with both legacy and modern projects.

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

<details>
<summary>🚀 Getting Started</summary>

1. Install the NuGet package (coming soon):
   ```powershell
   dotnet add package AtomicUI.WPF
   ```

2. Merge the theme resource dictionary:
   ```xml
   <ResourceDictionary>
     <ResourceDictionary.MergedDictionaries>
       <ResourceDictionary Source="pack://application:,,,/AtomicUI.WPF;component/Themes/AtomicUI.xaml" />
     </ResourceDictionary.MergedDictionaries>
   </ResourceDictionary>
   ```

3. (Optional) Replace your main window with `ModernWindow`:
   ```xml
   <ui:ModernWindow
       x:Class="MyApp.MainWindow"
       xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
       xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
       xmlns:ui="clr-namespace:AtomicUI.Controls;assembly=AtomicUI"
       Title="My App"
       Width="800"
       Height="600">
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

> 💡 Use `DynamicResource` for theme-aware brushes.  
> Dark & Light themes are included. Accent color customization is planned.  

</details>

---

## 🎨 Theming

- Dark & Light themes included (`Themes/Dark.xaml`, `Themes/Light.xaml`)  
- Use `DynamicResource` for color switching  
- Accent color customization planned for a future release  

---

## 📄 License

Commercial license required.  
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
- Pricing: [atomicapps.dev/pricing](https://atomicapps.dev/pricing)  
- YouTube: [AtomicAppsOfficial](https://www.youtube.com/@AtomicAppsOfficial)  
- X (Twitter): [@AtomicAppsUI](https://x.com/AtomicAppsUI)  
