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
* Go to the "Advanced" tab.
* Copy the content below to the text box under "Mod settings" and click "Save".

---

### Version 0.2.1

<details>
<summary>Content to import (click to expand)</summary>

```json
{
  "controlStyles[0].target": "Border#AcrylicBorder",
  "controlStyles[0].styles[0]": "Background:=$mbg",
  "controlStyles[0].styles[1]": "CornerRadius=$wcr",
  "controlStyles[0].styles[2]": "BorderThickness=$bt",
  "controlStyles[0].styles[3]": "BorderBrush=$bb",
  "controlStyles[1].target": "Windows.UI.Xaml.Controls.Border#AcrylicOverlay",
  "controlStyles[1].styles[0]": "Visibility=Collapsed",
  "controlStyles[2].target": "Windows.UI.Xaml.Controls.Border#RootGridDropShadow",
  "controlStyles[2].styles[0]": "CornerRadius=$wcr",
  "controlStyles[2].styles[1]": "Visibility=1",
  "controlStyles[3].target": "Button#ShowAllAppsButton",
  "controlStyles[3].styles[0]": "CornerRadius=$bcr",
  "controlStyles[4].target": "Button#CloseAllAppsButton",
  "controlStyles[4].styles[0]": "CornerRadius=$bcr",
  "controlStyles[5].target": "Windows.UI.Xaml.Controls.Grid#TopLevelSuggestionsContainer",
  "controlStyles[5].styles[0]": "RenderTransform:=<TranslateTransform X=\"-19\" Y=\"0\" />",
  "controlStyles[6].target": "Windows.UI.Xaml.Controls.GridViewItem > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[6].styles[0]": "CornerRadius=$mcr",
  "controlStyles[7].target": "Windows.UI.Xaml.Controls.Button#ShowMoreSuggestionsButton",
  "controlStyles[7].styles[0]": "CornerRadius=$bcr",
  "controlStyles[8].target": "Windows.UI.Xaml.Controls.Button#HideMoreSuggestionsButton",
  "controlStyles[8].styles[0]": "CornerRadius=$bcr",
  "controlStyles[8].styles[1]": "Margin=0,9,65,9",
  "controlStyles[9].target": "Windows.UI.Xaml.Controls.Button#HideMoreSuggestionsButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter > Windows.UI.Xaml.Controls.StackPanel > Windows.UI.Xaml.Controls.FontIcon > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBlock",
  "controlStyles[9].styles[0]": "RenderTransform:=<ScaleTransform ScaleX=\"0.76\" ScaleY=\"0.76\" />",
  "controlStyles[9].styles[1]": "Margin=0,5.9,0,0",
  "controlStyles[10].target": "Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot0 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[10].styles[0]": "CornerRadius=$mcr",
  "controlStyles[11].target": "Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot1 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[11].styles[0]": "CornerRadius=$mcr",
  "controlStyles[12].target": "Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot2 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[12].styles[0]": "CornerRadius=$mcr",
  "controlStyles[13].target": "Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot3 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[13].styles[0]": "CornerRadius=$mcr",
  "controlStyles[14].target": "Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot4 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[14].styles[0]": "CornerRadius=$mcr",
  "controlStyles[15].target": "Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot5 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[15].styles[0]": "CornerRadius=$mcr",
  "controlStyles[16].target": "Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot6 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[16].styles[0]": "CornerRadius=$mcr",
  "controlStyles[17].target": "Windows.UI.Xaml.Controls.GridViewItem#RecommendedItemRoot7 > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[17].styles[0]": "CornerRadius=$mcr",
  "controlStyles[18].target": "Windows.UI.Xaml.Controls.TextBlock#NoSuggestionsWithoutSettingsLink",
  "controlStyles[18].styles[0]": "RenderTransform:=<TranslateTransform X=\"19\" Y=\"0\" />",
  "controlStyles[19].target": "StartDocked.NavigationPaneView#NavigationPane",
  "controlStyles[19].styles[0]": "Margin=13,0,13,0",  
  "controlStyles[20].target": "StartDocked.NavigationPaneButton#UserTileButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[20].styles[0]": "CornerRadius=$wcr",
  "controlStyles[21].target": "Windows.UI.Xaml.Controls.Grid#UserTileIcon",
  "controlStyles[21].styles[0]": "RenderTransform:=<TranslateTransform X=\"-5\" Y=\"0\" />",  
  "controlStyles[22].target": "Windows.UI.Xaml.Controls.TextBlock#UserTileNameText",
  "controlStyles[22].styles[0]": "RenderTransform:=<TranslateTransform X=\"-5\" Y=\"0\" />",
  "controlStyles[23].target": "Grid#ContentBorder > Border#BackgroundBorder",
  "controlStyles[23].styles[0]": "CornerRadius=$wcr",
  "controlStyles[24].target": "StartDocked.PowerOptionsView#PowerButton > StartDocked.NavigationPaneButton#PowerButton > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[24].styles[0]": "CornerRadius=$wcr",

  "controlStyles[26].target": "StartMenu.ExpandedFolderList > Windows.UI.Xaml.Controls.Grid#Root > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.TextBox#ExpandedFolderNameTextBox > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BorderElement",
  "controlStyles[26].styles[0]": "CornerRadius=$mcr",
  "controlStyles[27].target": "Windows.UI.Xaml.Controls.GridView#FolderList > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.ScrollViewer#ScrollViewer > Windows.UI.Xaml.Controls.Border#Root > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.ScrollContentPresenter#ScrollContentPresenter > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.ContentControl > Windows.UI.Xaml.Controls.ItemsWrapGrid > Windows.UI.Xaml.Controls.GridViewItem > Windows.UI.Xaml.Controls.Border#ContentBorder > Windows.UI.Xaml.Controls.Grid#DroppedFlickerWorkaroundWrapper > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[27].styles[0]": "CornerRadius=$mcr",

  "controlStyles[28].target": "Windows.UI.Xaml.Controls.StackPanel#RootPanel > Windows.UI.Xaml.Controls.Button#Header > Windows.UI.Xaml.Controls.Border#Border",
  "controlStyles[28].styles[0]": "CornerRadius=$mcr",
  "controlStyles[29].target": "Windows.UI.Xaml.Controls.Grid#ContentBorder > Windows.UI.Xaml.Controls.Border#BorderBackground",
  "controlStyles[29].styles[0]": "CornerRadius=$mcr",
  "controlStyles[30].target": "ListView#ZoomAppsList > ItemsWrapGrid > ListViewItem > Grid#ContentBorder > Border#BorderBackground",

  "controlStyles[31].target": "Windows.UI.Xaml.Controls.Border#RightCompanionDropShadow",
  "controlStyles[31].styles[0]": "CornerRadius=$wcr",
  "controlStyles[31].styles[1]": "Visibility=1",
  "controlStyles[32].target": "Windows.UI.Xaml.Controls.Border#DropShadowDismissTarget",
  "controlStyles[32].styles[0]": "CornerRadius=$wcr",
  "controlStyles[32].styles[1]": "Visibility=1",
  "controlStyles[33].target": "Windows.UI.Xaml.Controls.ItemsStackPanel > Windows.UI.Xaml.Controls.ListViewItem > Windows.UI.Xaml.Controls.Grid#ContentBorder > Windows.UI.Xaml.Controls.Border#BorderBackground",
  "controlStyles[33].styles[0]": "CornerRadius=$mcr",
  "controlStyles[34].target": "Windows.UI.Xaml.Controls.Button#PrimaryActionBarButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter",
  "controlStyles[34].styles[0]": "CornerRadius=$mcr",
  "controlStyles[35].target": "Windows.UI.Xaml.Controls.Button#ActionBarOverflowButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter",
  "controlStyles[35].styles[0]": "CornerRadius=$mcr",

  "controlStyles[36].target": "Windows.UI.Xaml.Controls.MenuFlyoutPresenter > Windows.UI.Xaml.Controls.Border",
  "controlStyles[36].styles[0]": "Background:=$mbg",
  "controlStyles[36].styles[1]": "CornerRadius=$mcr",
  "controlStyles[36].styles[2]": "BorderThickness=$bt",
  "controlStyles[36].styles[3]": "BorderBrush=$bb",
  "controlStyles[37].target": "Windows.UI.Xaml.Controls.MenuFlyoutPresenter",
  "controlStyles[37].styles[0]": "CornerRadius:=$wcr",
  "controlStyles[37].styles[1]": "Shadow:=",
  "controlStyles[38].target": "Windows.UI.Xaml.Controls.MenuFlyoutItem",
  "controlStyles[38].styles[0]": "CornerRadius=$bcr",
  "controlStyles[39].target": "Windows.UI.Xaml.Controls.MenuFlyoutSubItem",
  "controlStyles[39].styles[0]": "CornerRadius=$bcr",
  "controlStyles[40].target": "JumpViewUI.JumpListListView#ItemList > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.ScrollViewer#ScrollViewer > Windows.UI.Xaml.Controls.Border#Root > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.ScrollContentPresenter#ScrollContentPresenter > Windows.UI.Xaml.Controls.ItemsPresenter > Windows.UI.Xaml.Controls.ItemsStackPanel > Windows.UI.Xaml.Controls.ListViewItem",
  "controlStyles[40].styles[0]": "CornerRadius=$bcr",
  "controlStyles[41].target": "Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot",
  "controlStyles[41].styles[0]": "Background:=$mbg",
  "controlStyles[41].styles[1]": "CornerRadius=$mcr",
  "controlStyles[41].styles[2]": "BorderThickness=$bt",
  "controlStyles[41].styles[3]": "BorderBrush=$bb",
  "controlStyles[41].styles[4]": "Shadow:=",

  "controlStyles[42].target": "Border#AppBorder",
  "controlStyles[42].styles[0]": "Background:=$mbg",
  "controlStyles[42].styles[1]": "CornerRadius=$wcr",
  "controlStyles[43].target": "Windows.UI.Xaml.Controls.Border#AppBorder",
  "controlStyles[43].styles[0]": "CornerRadius:=$wcr",
  "controlStyles[43].styles[1]": "BorderThickness=$bt",
  "controlStyles[43].styles[2]": "BorderBrush=$bb",
  "controlStyles[44].target": "Windows.UI.Xaml.Controls.Border#LayerBorder",
  "controlStyles[44].styles[0]": "Visibility=1",
  "controlStyles[45].target": "Border#dropshadow",
  "controlStyles[45].styles[0]": "CornerRadius:=$wcr",
  "controlStyles[45].styles[1]": "Visibility=1",

  "controlStyles[46].target": "ScrollViewer#MenuFlyoutPresenterScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > StackPanel",
  "controlStyles[46].styles[0]": "ChildrenTransitions:=$AnimationSettings",
  "controlStyles[47].target": "Grid#LayoutRoot",
  "controlStyles[47].styles[0]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",
  "controlStyles[48].target": "Border#BackgroundBorder",
  "controlStyles[48].styles[0]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",

  "styleConstants[0]": "mbg=<AcrylicBrush TintColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" FallbackColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" TintOpacity=\"0.0\" TintLuminosityOpacity=\"1.0\" Opacity=\"1\"/>",
  "styleConstants[1]": "bcr=10",
  "styleConstants[2]": "bbb=#13FFFFFF",
  "styleConstants[3]": "wcr=20",
  "styleConstants[4]": "mcr=15",
  "styleConstants[5]": "t=Transparent",
  "styleConstants[6]": "bb=#20FFFFFF",
  "styleConstants[7]": "nbb=<LinearGradientBrush x:Key=\"ShellTaskbarItemGradientStrokeColorSecondaryBrush\" MappingMode=\"Absolute\" StartPoint=\"0,0\" EndPoint=\"0,3\"><LinearGradientBrush.GradientStops><GradientStop Offset=\"0.33\" Color=\"#1AFFFFFF\" /><GradientStop Offset=\"1\" Color=\"#0FFFFFFF\" /></LinearGradientBrush.GradientStops></LinearGradientBrush>",
  "styleConstants[8]": "bt=1",
  "styleConstants[9]": "btn=#10FFFFFF",
  "styleConstants[10]": "bth=#15FFFFFF",
  "styleConstants[11]": "btp=#15FFFFFF",
  "styleConstants[12]": "nbt=<SolidColorBrush Color=\"{ThemeResource ControlFillColorDefault}\" />",
  "styleConstants[13]": "nbth=<SolidColorBrush Color=\"{ThemeResource ControlFillColorSecondary}\" />",
  "styleConstants[14]": "nbtp=<SolidColorBrush Color=\"{ThemeResource ControlFillColorTertiary}\" />",
  "styleConstants[15]": "1=<WindhawkBlur BlurAmount=\"15\" TintColor=\"#00000000\" />",
  "styleConstants[16]": "2=<AcrylicBrush TintColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" FallbackColor=\"{ThemeResource CardStrokeColorDefaultSolid}\" TintOpacity=\"0.0\" TintLuminosityOpacity=\"0.0\" Opacity=\"1\"/>",
  "controlStyles[25].target": "StartMenu.ExpandedFolderList > Windows.UI.Xaml.Controls.Grid#Root > Windows.UI.Xaml.Controls.Border",
  "controlStyles[25].styles[0]": "CornerRadius=$wcr",
  "controlStyles[25].styles[1]": "BorderThickness=$bt",
  "controlStyles[25].styles[2]": "BorderBrush=$bb",
  "controlStyles[25].styles[3]": "Shadow:=",
  "controlStyles[25].styles[4]": "Background:=$1",
  "styleConstants[17]": "AnimationSettings=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled=\"True\" FromHorizontalOffset=\"-50\" FromVerticalOffset=\"50\" /></TransitionCollection>"
}
```
</details>

---

### Version 0.3 (Early Access) Basic styling for the [redesigned Windows 11 Start menu](https://microsoft.design/articles/start-fresh-redesigning-windows-start-menu/)!

Reverse engineered [Fluid](https://github.com/ramensoftware/windows-11-start-menu-styling-guide/tree/main/Themes/Fluid) (All credits to [SandTechStuff](https://github.com/SandTechStuff)), applied and adapted its effects to the old Start Menu elements while I still had access to it.

It should work in both Start Menu versions.

**Known Issues**
- Missing changes in many small elements (redesigned Start menu)

Let me know of any issues.

## Manual installation

**⚠️ I'm transitioning from `json` to `yaml`, follow the updated guide below.**

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

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
