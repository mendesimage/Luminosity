# Luminosity theme for Windows 11 File Explorer Styler

**Author**: [mendes.image](https://github.com/mendesimage)

![Demonstration](fe.png)

## Intro
**Luminosity** is based on native Acrylic, using the maximum **TintLuminosityOpacity** value as its backdrop.

It's meant to be used with **Mica** or **MicaAlt** backdrops, with or without the **Translucent Windows** mod.

---

## General Information

The theme changes the following elements:

- Rounded tabs
- Transparent Command bars
- Transparent Address Bar and Search Box (Unless if in focus)
- Centralized Lower Command bar
- Transparent separator below lower Command bar
- Removed dropshadows
- Matching border brush on some UWP context menus
- Matching border brush and radius on some UWM tool tips

---

## Known Issues

I didn't know how to fix these. I couldn't find the correct target names, or I'm not sure if they can even be changed.

- Tooltips have no Acrylic
- Context menus doesn't have matching border radius
- Some Context menus doesn't have matching border brushes
- Context menus doesn't have matching backdrop
- Context menus inside context menus doesn't match anything

---

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

<details>
<summary>Content to import (click to expand)</summary>

```yaml
styleConstants:
  - mbg=<AcrylicBrush TintColor="{ThemeResource CardStrokeColorDefaultSolid}" FallbackColor="{ThemeResource CardStrokeColorDefaultSolid}" TintOpacity="0.0" TintLuminosityOpacity="1.0" Opacity="1"/>
  - bcr=10
  - bbb=#13FFFFFF
  - wcr=20
  - mcr=15
  - t=Transparent
  - bb=#20FFFFFF
  - bt=1
  - mbt=#10FFFFFF
  - mbth=#15FFFFFF
  - mbtp=#15FFFFFF
controlStyles:
  - target: TabViewItem > Grid#LayoutRoot
    styles:
      - CornerRadius=10
  - target: Button#AddButton
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="-1" />
  - target: Microsoft.UI.Xaml.Controls.Border#BottomBorderLine
    styles:
      - Visibility=Collapsed
  - target: Grid#TabContainerGrid > Border#LeftBottomBorderLine
    styles:
      - Visibility=Collapsed
  - target: Grid#TabContainerGrid > Border#RightBottomBorderLine
    styles:
      - Visibility=Collapsed
  - target: Microsoft.UI.Xaml.Controls.Grid#NavigationBarControlGrid
    styles:
      - Background:=$t
  - target: Microsoft.UI.Xaml.Controls.Grid#PART_LayoutRoot
    styles:
      - ''
  - target: Microsoft.UI.Xaml.Controls.AutoSuggestBox#FileExplorerSearchBox > Microsoft.UI.Xaml.Controls.Grid#LayoutRoot > Microsoft.UI.Xaml.Controls.TextBox#TextBox
    styles:
      - ''
  - target: Microsoft.UI.Xaml.Controls.Grid#CommandBarControlRootGrid
    styles:
      - Background:=$t
      - BorderBrush:=$t
  - target: Microsoft.UI.Xaml.Controls.CommandBar#FileExplorerCommandBar
    styles:
      - Background:=$t
      - RenderTransform:=<TranslateTransform X="0" Y="-5" />
      - HorizontalAlignment=Center
  - target: Microsoft.UI.Xaml.Controls.CommandBar#FileExplorerSecondaryCommandBar > Microsoft.UI.Xaml.Controls.Grid#LayoutRoot > Microsoft.UI.Xaml.Controls.Grid#ContentRoot
    styles:
      - Visibility=Collapsed
  - target: Microsoft.UI.Xaml.Controls.Grid#HomeViewRootGrid
    styles:
      - Background:=$t
  - target: FileExplorerExtensions.GalleryViewControl - GalleryViewControl
    styles:
      - Visibility=Collapsed
  - target: FileExplorerExtensions.GalleryViewControl#GalleryViewControl > Grid
    styles:
      - Background:=$t
  - target: TabViewItem > Grid#LayoutRoot
    styles:
      - CornerRadius=$mcr
      - BorderThickness=0
      - BorderBrush=$t
  - target: Button#CloseButton
    styles:
      - CornerRadius=$bcr
  - target: Button#AddButton
    styles:
      - CornerRadius=$bcr
  - target: TabViewItem > Grid#LayoutRoot@CommonStates
    styles:
      - Background@Normal:=$t
      - Background@PointerOver:=#02FFFFFF
      - Background@Selected:=#05FFFFFF
      - Background@PointerOverSelected:=$mbth
      - Background@PressedSelected:=$mbth
  - target: Microsoft.UI.Xaml.Controls.Grid#PART_LayoutRoot
    styles:
      - CornerRadius=14
      - BorderBrush:=$bbb
  - target: Microsoft.UI.Xaml.Controls.Primitives.ToggleButton#PART_RootChevronButton
    styles:
      - CornerRadius=$bcr
  - target: Microsoft.UI.Xaml.Controls.TextBox - TextBox > Microsoft.UI.Xaml.Controls.Grid > Microsoft.UI.Xaml.Controls.Border#BorderElement > Microsoft.UI.Xaml.Controls.ScrollViewer#ContentElement > Microsoft.UI.Xaml.Controls.Border#Root > Microsoft.UI.Xaml.Controls.Grid > Microsoft.UI.Xaml.Controls.ScrollContentPresenter#ScrollContentPresenter > Microsoft.UI.Xaml.Internal.TextBoxView
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="1" />
  - target: Microsoft.UI.Xaml.Controls.Primitives.ToggleButton#PART_RootChevronButton
    styles:
      - CornerRadius=8
  - target: Microsoft.UI.Xaml.Controls.AutoSuggestBox#FileExplorerSearchBox > Microsoft.UI.Xaml.Controls.Grid#LayoutRoot > Microsoft.UI.Xaml.Controls.TextBox#TextBox
    styles:
      - Background:=$mbt
      - CornerRadius=$mcr
      - BorderBrush:=$bbb
      - Margin=0,-0.3,0,-0.75
  - target: Microsoft.UI.Xaml.Controls.Button#MoreButton > Microsoft.UI.Xaml.Controls.Grid@CommonStates
    styles:
      - CornerRadius@PointerOver:=$bcr
      - CornerRadius@Pressed:=$bcr
  - target: MenuFlyoutPresenter > Border
    styles:
      - BorderThickness:=$bt
      - BorderBrush:=$bb
      - CornerRadius:=$mcr
  - target: MenuFlyoutPresenter
    styles:
      - BorderThickness:=$bt
      - BorderBrush:=$bb
      - CornerRadius:=$mcr
  - target: Microsoft.UI.Xaml.Controls.Primitives.CommandBarFlyoutCommandBar
    styles:
      - BorderThickness:=$bt
      - BorderBrush:=$bb
      - CornerRadius:=$mcr
  - target: Microsoft.UI.Xaml.Controls.RadioMenuFlyoutItem
    styles:
      - CornerRadius=$bcr
  - target: Microsoft.UI.Xaml.Controls.Border#AppBarButtonInnerBorder
    styles:
      - CornerRadius=$bcr
  - target: Microsoft.UI.Xaml.Controls.MenuFlyoutItem
    styles:
      - CornerRadius=$bcr
  - target: Microsoft.UI.Xaml.Controls.MenuFlyoutSubItem
    styles:
      - CornerRadius=$bcr
  - target: ToolTip
    styles:
      - Background:=$mbg
      - CornerRadius:=$mcr
      - BorderThickness:=$bt
      - BorderBrush:=$bb
  - target: Microsoft.UI.Xaml.Controls.Primitives.CommandBarFlyoutCommandBar > Grid#LayoutRoot > Grid#OuterContentRoot > Grid#ContentRoot > Grid#PrimaryItemsRoot
    styles:
      - ''
  - target: ScrollViewer#MenuFlyoutPresenterScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > StackPanel
    styles:
      - ChildrenTransitions:=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled="True" FromHorizontalOffset="-50" FromVerticalOffset="50" /></TransitionCollection>
  - target: Grid#LayoutRoot
    styles:
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.100" />
  - target: Border#BackgroundBorder
    styles:
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.100" />
  - target: TabViewItem > Grid#LayoutRoot > Canvas > Microsoft.UI.Xaml.Shapes.Path#SelectedBackgroundPath
    styles:
      - Fill:=$mbt
```

</details>
