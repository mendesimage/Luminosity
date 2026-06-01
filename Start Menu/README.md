# Luminosity theme for Windows 11 Start Menu Styler

**Author**: [mendes.image](https://github.com/mendesimage)

![Demonstration](1.png)

> [!IMPORTANT]
> Development for the [redesigned Windows 11 Start menu](https://microsoft.design/articles/start-fresh-redesigning-windows-start-menu/) just started! Available in the version 0.3 at the end of the page. **It have different installation guide**!

## Intro
**Luminosity** is based on native Acrylic, using the maximum **TintLuminosityOpacity** value as its backdrop.

It's meant to be used with **Mica** or **MicaAlt** backdrops, with or without the **Translucent Windows** mod.

---

## Optional settings

### Clear Acrylic App Folder Background

If you prefer a Clear Acrylic look for the Folder's background instead of the default blur, you can change one value in the JSON file:

Find this line at the end:
```
"controlStyles[24].styles[4]": "Background:=$1"
```

Replace the **"Background"** value from ```$1``` to ```$2```, like this:
```
"controlStyles[24].styles[4]": "Background:=$2"
```

### Animations Guide

To customize the animations, look for the last line `"styleConstants[17]": "AnimationSettings=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled=\"True\" FromHorizontalOffset=\"-50\" FromVerticalOffset=\"50\" /></TransitionCollection>"`

- For all items to display immediately, set `IsStaggeringEnabled=\"True\"` to `False`.

- `FromHorizontalOffset` and `FromVerticalOffset` are the directions where the items come from.
  - Horizontal **Positive** values is **Right**, **Negative** is **Left**.
  - Vertical **Positive** values is **Down**, **Negative** is **Up**.
  
---

## General Information

The theme changes the following elements:

- Start and Search Menu
- App Group Backdrops
- Rounded several buttons
- Context menus

---

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

---

### Version 0.2.2

<details>
<summary>Content to import (click to expand)</summary>

```yaml
styleConstants:
  - mbg=<WindhawkBlur BlurAmount="30" TintColor="{ThemeResource CardStrokeColorDefaultSolid}" TintOpacity="0.0" TintLuminosityOpacity="1.0" TintSaturation="1.0" NoiseDensity="1.0" NoiseOpacity="0.1" />
  - bcr=10
  - bbb=#13FFFFFF
  - wcr=20
  - mcr=15
  - t=Transparent
  - bb=#20FFFFFF
  - nbb=<LinearGradientBrush x:Key="ShellTaskbarItemGradientStrokeColorSecondaryBrush" MappingMode="Absolute" StartPoint="0,0" EndPoint="0,3"><LinearGradientBrush.GradientStops><GradientStop Offset="0.33" Color="#1AFFFFFF" /><GradientStop Offset="1" Color="#0FFFFFFF" /></LinearGradientBrush.GradientStops></LinearGradientBrush>
  - bt=1
  - btn=#10FFFFFF
  - bth=#15FFFFFF
  - btp=#15FFFFFF
  - nbt=<SolidColorBrush Color="{ThemeResource ControlFillColorDefault}" />
  - nbth=<SolidColorBrush Color="{ThemeResource ControlFillColorSecondary}" />
  - nbtp=<SolidColorBrush Color="{ThemeResource ControlFillColorTertiary}" />
  - 1=<WindhawkBlur BlurAmount="15" TintColor="#00000000" />
  - 2=<AcrylicBrush TintColor="{ThemeResource CardStrokeColorDefaultSolid}" FallbackColor="{ThemeResource CardStrokeColorDefaultSolid}" TintOpacity="0.0" TintLuminosityOpacity="0.0" Opacity="1"/>
  - AnimationSettings=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled="True" FromHorizontalOffset="-50" FromVerticalOffset="50" /></TransitionCollection>
controlStyles:
  - target: Border#AcrylicBorder
    styles:
      - Background:=$mbg
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
  - target: Windows.UI.Xaml.Controls.Border#AcrylicOverlay
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Border#RootGridDropShadow
    styles:
      - CornerRadius=$wcr
      - Visibility=1
  - target: Button#ShowAllAppsButton
    styles:
      - CornerRadius=$bcr
  - target: Button#CloseAllAppsButton
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.Grid#TopLevelSuggestionsContainer
    styles:
      - RenderTransform:=<TranslateTransform X="-19" Y="0" />
  - target: Windows.UI.Xaml.Controls.GridViewItem > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.Button#ShowMoreSuggestionsButton
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.Button#HideMoreSuggestionsButton
    styles:
      - CornerRadius=$bcr
      - Margin=0,9,65,9
  - target: Windows.UI.Xaml.Controls.Button#HideMoreSuggestionsButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.FontIcon > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBlock
    styles:
      - RenderTransform:=<ScaleTransform ScaleX="0.76" ScaleY="0.76" />
      - Margin=0,5.9,0,0
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot0 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot1 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot2 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot3 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot4 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot5 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot6 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot7 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.TextBlock#NoSuggestionsWithoutSettingsLink
    styles:
      - RenderTransform:=<TranslateTransform X="19" Y="0" />
  - target: StartDocked.NavigationPaneView#NavigationPane
    styles:
      - Margin=13,0,13,0
  - target: StartDocked.NavigationPaneButton#UserTileButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$wcr
  - target: Windows.UI.Xaml.Controls.Grid#UserTileIcon
    styles:
      - RenderTransform:=<TranslateTransform X="-5" Y="0" />
  - target: Windows.UI.Xaml.Controls.TextBlock#UserTileNameText
    styles:
      - RenderTransform:=<TranslateTransform X="-5" Y="0" />
  - target: Grid#ContentBorder > Border#BackgroundBorder
    styles:
      - CornerRadius=$wcr
  - target: StartDocked.PowerOptionsView#PowerButton > StartDocked.NavigationPaneButton#PowerButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$wcr
  - target: StartMenu.ExpandedFolderList > Windows.UI.Xaml.Controls.Grid#Root > Windows.UI.Xaml.Controls.Border
    styles:
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
      - Background:=$1
  - target: StartMenu.ExpandedFolderList > Windows.UI.Xaml.Controls.Grid#Root > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBox#ExpandedFolderNameTextBox > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BorderElement
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridView#FolderList > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.ScrollViewer#ScrollViewer > Windows.UI.Xaml.Controls.Border#Root > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.ScrollContentPresenter#ScrollContentPresenter > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.ContentControl > Windows.UI.Xaml.Controls.ItemsWrapGrid > Windows.UI.Xaml.Controls.GridViewItem > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.StackPanel#RootPanel > Windows.UI.Xaml.Controls.Button#Header > Windows.UI.Xaml.Controls.Border#Border
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.Grid#ContentBorder > Windows.UI.Xaml.Controls.Border#BorderBackground
    styles:
      - CornerRadius=$mcr
  - target: ListView#ZoomAppsList > ItemsWrapGrid > ListViewItem > Grid#ContentBorder > Border#BorderBackground
    styles:
      - ''
  - target: Windows.UI.Xaml.Controls.Border#RightCompanionDropShadow
    styles:
      - CornerRadius=$wcr
      - Visibility=1
  - target: Windows.UI.Xaml.Controls.Border#DropShadowDismissTarget
    styles:
      - CornerRadius=$wcr
      - Visibility=1
  - target: Windows.UI.Xaml.Controls.ItemsStackPanel > Windows.UI.Xaml.Controls.ListViewItem > Windows.UI.Xaml.Controls.Grid#ContentBorder > Windows.UI.Xaml.Controls.Border#BorderBackground
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.Button#PrimaryActionBarButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.Button#ActionBarOverflowButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.MenuFlyoutPresenter > Windows.UI.Xaml.Controls.Border
    styles:
      - Background:=$mbg
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
  - target: Windows.UI.Xaml.Controls.MenuFlyoutPresenter
    styles:
      - CornerRadius:=$wcr
      - Shadow:=
  - target: Windows.UI.Xaml.Controls.MenuFlyoutItem
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.MenuFlyoutSubItem
    styles:
      - CornerRadius=$bcr
  - target: JumpViewUI.JumpListListView#ItemList > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.ScrollViewer#ScrollViewer > Windows.UI.Xaml.Controls.Border#Root > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.ScrollContentPresenter#ScrollContentPresenter > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.ItemsStackPanel > Windows.UI.Xaml.Controls.ListViewItem
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot
    styles:
      - Background:=$mbg
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: Border#AppBorder
    styles:
      - Background:=$mbg
      - CornerRadius=$wcr
  - target: Windows.UI.Xaml.Controls.Border#AppBorder
    styles:
      - CornerRadius:=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
  - target: Windows.UI.Xaml.Controls.Border#LayerBorder
    styles:
      - Visibility=1
  - target: Border#dropshadow
    styles:
      - CornerRadius:=$wcr
      - Visibility=1
  - target: ScrollViewer#MenuFlyoutPresenterScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > StackPanel
    styles:
      - ChildrenTransitions:=$AnimationSettings
  - target: Grid#LayoutRoot
    styles:
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.100" />
  - target: Border#BackgroundBorder
    styles:
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.100" />
```
</details>

---

### Version 0.3 (Early Access) Basic styling for the [redesigned Windows 11 Start menu](https://microsoft.design/articles/start-fresh-redesigning-windows-start-menu/)!

Reverse engineered [Fluid](https://github.com/ramensoftware/windows-11-start-menu-styling-guide/tree/main/Themes/Fluid) (All credits to [SandTechStuff](https://github.com/SandTechStuff)), applied and adapted its effects to the old Start Menu elements while I still had access to it.

It should work in both Start Menu versions.

**Known Issues**
- Missing changes in many small elements (redesigned Start menu)

Let me know of any issues.

<details>
<summary>Content to import (click to expand)</summary>

```yaml
styleConstants:
  - AccentColor=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight2}" Opacity="1.0" />
  - AnimationSettings=IsStaggeringEnabled="True" FromHorizontalOffset="-50" FromVerticalOffset="50"
  - mbg=<WindhawkBlur BlurAmount="30" TintColor="{ThemeResource CardStrokeColorDefaultSolid}" TintOpacity="0.0" TintLuminosityOpacity="1.0" TintSaturation="1.0" NoiseDensity="1.0" NoiseOpacity="0.1" />
  - bcr=10
  - wcr=20
  - mcr=15
  - t=Transparent
  - bb=#20FFFFFF
  - bt=1
  - nbb=<LinearGradientBrush x:Key="ShellTaskbarItemGradientStrokeColorSecondaryBrush" MappingMode="Absolute" StartPoint="0,0" EndPoint="0,3"><LinearGradientBrush.GradientStops><GradientStop Offset="0.33" Color="#1AFFFFFF" /><GradientStop Offset="1" Color="#0FFFFFFF" /></LinearGradientBrush.GradientStops></LinearGradientBrush>
  - nbt=<SolidColorBrush Color="{ThemeResource ControlFillColorDefault}" />
  - nbth=<SolidColorBrush Color="{ThemeResource ControlFillColorSecondary}" />
  - nbtp=<SolidColorBrush Color="{ThemeResource ControlFillColorTertiary}" />
  - fa=100
  - 1=<WindhawkBlur BlurAmount="15" TintColor="#00000000" />
  - 2=<AcrylicBrush TintColor="{ThemeResource CardStrokeColorDefaultSolid}" FallbackColor="{ThemeResource CardStrokeColorDefaultSolid}" TintOpacity="0.0" TintLuminosityOpacity="0.0" Opacity="1"/>
controlStyles:
  - target: Border#AcrylicBorder
    styles:
      - Background:=$mbg
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
  - target: Windows.UI.Xaml.Controls.Border#AcrylicOverlay
    styles:
      - Visibility=Collapsed
  - target: Windows.UI.Xaml.Controls.Border#RootGridDropShadow
    styles:
      - CornerRadius=$wcr
      - Visibility=1
  - target: Border#StartDropShadow
    styles:
      - CornerRadius=$wcr
      - Visibility=1
  - target: Primitives.ToggleButton#ShowHideCompanion > Border@CommonStates
    styles:
      - Margin=-1.5
      - Background@Normal:=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - Background@Disabled:=$t
      - Background@Checked:=$t
      - Background@CheckedPointerOver:=$nbth
      - Background@CheckedPressed:=$nbtp
      - Background@CheckedDisabled:=$t
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BorderBrush@Disabled:=$t
      - BorderBrush@Checked:=$t
      - BorderBrush@CheckedPointerOver:=$nbb
      - BorderBrush@CheckedPressed:=$nbb
      - BorderBrush@CheckedDisabled:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: Primitives.ToggleButton#ShowHideCompanion > Border@CommonStates > ContentPresenter#ContentPresenter
    styles:
      - Margin=-1.5
      - Background@Normal:=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - Background@Disabled:=$t
      - Background@Checked:=$t
      - Background@CheckedPointerOver:=$nbth
      - Background@CheckedPressed:=$nbtp
      - Background@CheckedDisabled:=$t
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BorderBrush@Disabled:=$t
      - BorderBrush@Checked:=$t
      - BorderBrush@CheckedPointerOver:=$nbb
      - BorderBrush@CheckedPressed:=$nbb
      - BorderBrush@CheckedDisabled:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: Button#ShowAllAppsButton
    styles:
      - CornerRadius=$bcr
  - target: Button#CloseAllAppsButton
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.Grid#TopLevelSuggestionsContainer
    styles:
      - RenderTransform:=<TranslateTransform X="0" Y="0" />
  - target: Windows.UI.Xaml.Controls.GridViewItem > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.Button#ShowMoreSuggestionsButton
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.Button#HideMoreSuggestionsButton
    styles:
      - CornerRadius=$bcr
      - Margin=0,9,65,9
  - target: Windows.UI.Xaml.Controls.Button#HideMoreSuggestionsButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.FontIcon > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBlock
    styles:
      - RenderTransform:=<ScaleTransform ScaleX="0.76" ScaleY="0.76" />
      - Margin=0,5,0,0
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot0 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot1 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot2 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot3 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot4 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot5 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot6 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot7 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.TextBlock#NoSuggestionsWithoutSettingsLink
    styles:
      - RenderTransform:=<TranslateTransform X="19" Y="0" />
  - target: DropDownButton#ViewSelectionButton > Grid#RootGrid@CommonStates
    styles:
      - CornerRadius=$bcr
      - Background@Normal:=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - Background@Disabled:=$t
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BorderBrush@Disabled:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: ToggleMenuFlyoutItem
    styles:
      - CornerRadius=$bcr
  - target: StartMenu.CategoryControl > Grid#RootGrid > Border
    styles:
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$t
      - Shadow:=
  - target: Button#LogoContainer > ContentPresenter > Grid@CommonStates > Border#BackgroundBorder
    styles:
      - CornerRadius=$bcr
      - Background@Normal:=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - Background@Disabled:=$t
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BorderBrush@Disabled:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: StartDocked.NavigationPaneView#NavigationPane
    styles:
      - Margin=13,0,13,0
  - target: StartDocked.NavigationPaneButton#UserTileButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$wcr
  - target: Windows.UI.Xaml.Controls.Grid#UserTileIcon
    styles:
      - RenderTransform:=<TranslateTransform X="-5" Y="0" />
  - target: Windows.UI.Xaml.Controls.TextBlock#UserTileNameText
    styles:
      - RenderTransform:=<TranslateTransform X="-5" Y="0" />
  - target: Grid#ContentBorder > Border#BackgroundBorder
    styles:
      - CornerRadius=$wcr
  - target: StartDocked.PowerOptionsView#PowerButton > StartDocked.NavigationPaneButton#PowerButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$wcr
  - target: StartMenu.ExpandedFolderList > Windows.UI.Xaml.Controls.Grid#Root > Windows.UI.Xaml.Controls.Border
    styles:
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
      - Background:=$1
  - target: StartMenu.FolderModal#StartFolderModal > Grid#Root > Border
    styles:
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
      - Background:=$1
  - target: StartMenu.ExpandedFolderList > Windows.UI.Xaml.Controls.Grid#Root > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBox#ExpandedFolderNameTextBox > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BorderElement
    styles:
      - Background:=$t
      - BorderBrush=$t
  - target: Windows.UI.Xaml.Controls.GridView#FolderList > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.ScrollViewer#ScrollViewer > Windows.UI.Xaml.Controls.Border#Root > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.ScrollContentPresenter#ScrollContentPresenter > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.ContentControl > Windows.UI.Xaml.Controls.ItemsWrapGrid > Windows.UI.Xaml.Controls.GridViewItem > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - CornerRadius=$mcr
  - target: TextBox#MutableFolderNameTextBox
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.StackPanel#RootPanel > Windows.UI.Xaml.Controls.Button#Header > Windows.UI.Xaml.Controls.Border#Border
    styles:
      - CornerRadius=$mcr
  - target: GridViewHeaderItem > Border > ContentPresenter#ContentPresenter > Button#Header > Border#Border
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.Grid#ContentBorder > Windows.UI.Xaml.Controls.Border#BorderBackground
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.Border#RightCompanionDropShadow
    styles:
      - CornerRadius=$wcr
      - Visibility=1
  - target: Windows.UI.Xaml.Controls.Border#DropShadowDismissTarget
    styles:
      - CornerRadius=$wcr
      - Visibility=1
  - target: Windows.UI.Xaml.Controls.ItemsStackPanel > Windows.UI.Xaml.Controls.ListViewItem > Windows.UI.Xaml.Controls.Grid#ContentBorder > Windows.UI.Xaml.Controls.Border#BorderBackground
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.Button#PrimaryActionBarButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter
    styles:
      - CornerRadius=$mcr
  - target: Windows.UI.Xaml.Controls.Button#ActionBarOverflowButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter
    styles:
      - CornerRadius=$mcr
  - target: Button#PrimaryActionBarButton > Grid@CommonStates > Border#BackgroundBorder
    styles:
      - CornerRadius=$wcr
      - Background@Normal:=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - Background@Disabled:=$t
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BorderBrush@Disabled:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: Button#ActionBarOverflowButton > Grid@CommonStates > Border#BackgroundBorder
    styles:
      - CornerRadius=$wcr
      - Background@Normal:=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - Background@Disabled:=$t
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BorderBrush@Disabled:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: Windows.UI.Xaml.Controls.MenuFlyoutPresenter > Windows.UI.Xaml.Controls.Border
    styles:
      - Background:=$mbg
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
  - target: Windows.UI.Xaml.Controls.MenuFlyoutPresenter
    styles:
      - CornerRadius:=$wcr
      - Shadow:=
  - target: Windows.UI.Xaml.Controls.MenuFlyoutItem
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.MenuFlyoutSubItem
    styles:
      - CornerRadius=$bcr
  - target: JumpViewUI.JumpListListView#ItemList > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.ScrollViewer#ScrollViewer > Windows.UI.Xaml.Controls.Border#Root > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.ScrollContentPresenter#ScrollContentPresenter > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.ItemsStackPanel > Windows.UI.Xaml.Controls.ListViewItem
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot
    styles:
      - Background:=$mbg
      - CornerRadius=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: Border#AppBorder
    styles:
      - Background:=$mbg
      - CornerRadius=$wcr
  - target: Windows.UI.Xaml.Controls.Border#AppBorder
    styles:
      - CornerRadius:=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
  - target: Windows.UI.Xaml.Controls.Border#LayerBorder
    styles:
      - Visibility=1
  - target: Border#dropshadow
    styles:
      - CornerRadius:=$wcr
      - Visibility=1
  - target: ScrollViewer#MenuFlyoutPresenterScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > StackPanel
    styles:
      - ChildrenTransitions:=<TransitionCollection><EntranceThemeTransition $AnimationSettings /></TransitionCollection>
  - target: Grid#LayoutRoot
    styles:
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: Border#BackgroundBorder
    styles:
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: StartDocked.SearchBoxToggleButton#StartMenuSearchBox > Windows.UI.Xaml.Controls.Grid@CommonStates > Windows.UI.Xaml.Controls.Border#BorderElement
    styles:
      - Background@Checked:=$t
      - Background@CheckedPointerOver:=$t
      - Background@CheckedPressed:=$t
      - Background@CheckedDisabled:=$t
      - Background@Normal:=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - Background@Disabled:=$t
      - BorderThickness=2
      - BorderBrush@Checked:=$t
      - BorderBrush@CheckedPointerOver:=$t
      - BorderBrush@CheckedPressed:=$t
      - BorderBrush@CheckedDisabled:=$t
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BorderBrush@Disabled:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: StartMenu.SearchBoxToggleButton#SearchBoxToggleButton > Grid@CommonStates > Border#BorderElement
    styles:
      - Background@Checked:=$t
      - Background@CheckedPointerOver:=$t
      - Background@CheckedPressed:=$t
      - Background@CheckedDisabled:=$t
      - Background@Normal:=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - Background@Disabled:=$t
      - BorderThickness=2
      - BorderBrush@Checked:=$t
      - BorderBrush@CheckedPointerOver:=$t
      - BorderBrush@CheckedPressed:=$t
      - BorderBrush@CheckedDisabled:=$t
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BorderBrush@Disabled:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: Button > ContentPresenter#ContentPresenter@CommonStates
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: Border#ContentBorder@CommonStates > Grid > Border#BackgroundBorder
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: Button#ShowMoreSuggestionsButton > Grid@CommonStates > Border#BackgroundBorder
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: Button#HideMoreSuggestionsButton > Grid@CommonStates > Border#BackgroundBorder
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: StartDocked.NavigationPaneButton#UserTileButton > Windows.UI.Xaml.Controls.Grid@CommonStates > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: Grid#ContentBorder@CommonStates > Border#BackgroundBorder
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: StartDocked.PowerOptionsView#PowerButton > StartDocked.NavigationPaneButton#PowerButton > Windows.UI.Xaml.Controls.Grid@CommonStates > Windows.UI.Xaml.Controls.Border#BackgroundBorder
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: Windows.UI.Xaml.Controls.TextBox#ExpandedFolderNameTextBox > Windows.UI.Xaml.Controls.Grid@CommonStates
    styles:
      - Background@Normal:=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - Background@Focused:=$nbt
      - CornerRadius:=$mcr
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BorderBrush@Focused:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: TextBox#MutableFolderNameTextBox > Grid@CommonStates
    styles:
      - Background@Normal:=$t
      - Background@PointerOver:=$nbth
      - Background@Focused:=$nbt
      - Background@Disabled:=$t
      - CornerRadius:=$mcr
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Focused:=$t
      - BorderBrush@Disabled:=$t
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: Windows.UI.Xaml.Controls.StackPanel#RootPanel > Windows.UI.Xaml.Controls.Button#Header > Windows.UI.Xaml.Controls.Border#Border@CommonStates
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: GridViewHeaderItem > Border > ContentPresenter#ContentPresenter > Button#Header > Border#Border@CommonStates
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - Background@Disabled:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BorderBrush@Disabled:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: Windows.UI.Xaml.Controls.Grid#ContentBorder@CommonStates > Windows.UI.Xaml.Controls.Border#BorderBackground
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: Windows.UI.Xaml.Controls.ListViewItem > Windows.UI.Xaml.Controls.Grid#ContentBorder@CommonStates > Windows.UI.Xaml.Controls.Border#BorderBackground
    styles:
      - Background@Normal=$t
      - Background@PointerOver:=$nbth
      - Background@Pressed:=$nbtp
      - BorderThickness=2
      - BorderBrush@Normal:=$t
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Pressed:=$nbb
      - BackgroundSizing=InnerBorderEdge
  - target: Cortana.UI.Views.CortanaRichSearchBox#SearchTextBox > Windows.UI.Xaml.Controls.Grid@CommonStates > Windows.UI.Xaml.Controls.Border#BorderElement
    styles:
      - Background@Focused:=$nbt
      - Background@Normal:=$nbt
      - Background@PointerOver:=$nbth
      - Background@Disabled:=$nbt
      - BorderThickness=2
      - BorderBrush@Focused:=$nbb
      - BorderBrush@Normal:=$nbb
      - BorderBrush@PointerOver:=$nbb
      - BorderBrush@Disabled:=$nbb
      - BackgroundSizing=InnerBorderEdge
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.$fa" />
  - target: Windows.UI.Xaml.Controls.Border#TaskbarSearchBackground
    styles:
      - Background:=$t
      - BorderBrush:=$t
```
</details>
