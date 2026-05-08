# Luminosity theme for Windows 11 Start Menu Styler

**Author**: [mendes.image](https://github.com/mendesimage)

![Demonstration](1.png)

> [!IMPORTANT]
> It can have __**issues**__ with the [redesigned Windows 11 Start menu](https://microsoft.design/articles/start-fresh-redesigning-windows-start-menu/)! 
> I currently don't have access to the new Start Menu.

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

## Full Luminosity Theme

For that, download the listed mods and select "**Luminosity**" on each.
- Windows 11 Taskbar Styler
- Windows 11 Start Menu Styler
- Windows 11 Notification Center Styler
- Windows 11 File Explorer Styler

I also highly recommend **Translucent Windows** with **Mica** or **MicaAlt** selected as backdrop.

---

## Theme selection

The theme is integrated into the mod and can simply be selected from the mod's
settings:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme and save the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Taskbar Styler mod in Windhawk.
* Go to the "Advanced" tab.
* Copy the content below to the text box under "Mod settings" and click "Save".

---

### Stable Version

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

### Final Version (Usable - Early Access)

Reverse engineered [Fluid](https://github.com/ramensoftware/windows-11-start-menu-styling-guide/tree/main/Themes/Fluid) (All credits to [SandTechStuff](https://github.com/SandTechStuff)), applied and adapted its effects to the old Start Menu elements while I still have access to it.

**Known Issues**
- No known issues at the moment

Let me know of any issues. 
**It still have issues with the [Redesigned Start Menu](https://microsoft.design/articles/start-fresh-redesigning-windows-start-menu/)** and I can't fix these yet.

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
  "controlStyles[9].styles[1]": "Margin=0,5,0,0",
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
  "controlStyles[26].styles[0]": "Background:=$t",
  "controlStyles[26].styles[1]": "BorderBrush=$t",
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

  "controlStyles[49].target": "StartDocked.SearchBoxToggleButton#StartMenuSearchBox > Windows.UI.Xaml.Controls.Grid@CommonStates > Windows.UI.Xaml.Controls.Border#BorderElement",
  "controlStyles[49].styles[0]": "Background@Checked:=$t",
  "controlStyles[49].styles[1]": "Background@CheckedPointerOver:=$t",
  "controlStyles[49].styles[2]": "Background@CheckedPressed:=$t",
  "controlStyles[49].styles[3]": "Background@CheckedDisabled:=$t",
  "controlStyles[49].styles[4]": "Background@Normal:=$t",
  "controlStyles[49].styles[5]": "Background@PointerOver:=$nbth",
  "controlStyles[49].styles[6]": "Background@Pressed:=$nbtp",
  "controlStyles[49].styles[7]": "BorderThickness=2",
  "controlStyles[49].styles[8]": "BorderBrush@Checked:=$t",
  "controlStyles[49].styles[9]": "BorderBrush@CheckedPointerOver:=$t",
  "controlStyles[49].styles[10]": "BorderBrush@CheckedPressed:=$t",
  "controlStyles[49].styles[11]": "BorderBrush@CheckedDisabled:=$t",
  "controlStyles[49].styles[12]": "BorderBrush@Normal:=$t",
  "controlStyles[49].styles[13]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[49].styles[14]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[49].styles[15]": "BackgroundSizing=InnerBorderEdge",
  "controlStyles[49].styles[16]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",

  "controlStyles[50].target": "Button > ContentPresenter#ContentPresenter@CommonStates",
  "controlStyles[50].styles[0]": "Background@Normal=$t",
  "controlStyles[50].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[50].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[50].styles[3]": "BorderThickness=2",
  "controlStyles[50].styles[4]": "BorderBrush@Normal:=$t",
  "controlStyles[50].styles[5]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[50].styles[6]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[50].styles[7]": "BackgroundSizing=InnerBorderEdge",
  "controlStyles[51].target": "Border#ContentBorder@CommonStates > Grid > Border#BackgroundBorder",
  "controlStyles[51].styles[0]": "Background@Normal=$t",
  "controlStyles[51].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[51].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[51].styles[3]": "BorderThickness=2",
  "controlStyles[51].styles[4]": "BorderBrush@Normal:=$t",
  "controlStyles[51].styles[5]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[51].styles[6]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[51].styles[7]": "BackgroundSizing=InnerBorderEdge",
  "controlStyles[52].target": "Button#ShowMoreSuggestionsButton > Grid@CommonStates > Border#BackgroundBorder",
  "controlStyles[52].styles[0]": "Background@Normal=$t",
  "controlStyles[52].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[52].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[52].styles[3]": "BorderThickness=2",
  "controlStyles[52].styles[4]": "BorderBrush@Normal:=$t",
  "controlStyles[52].styles[5]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[52].styles[6]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[52].styles[7]": "BackgroundSizing=InnerBorderEdge",
  "controlStyles[53].target": "Button#HideMoreSuggestionsButton > Grid@CommonStates > Border#BackgroundBorder",
  "controlStyles[53].styles[0]": "Background@Normal=$t",
  "controlStyles[53].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[53].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[53].styles[3]": "BorderThickness=2",
  "controlStyles[53].styles[4]": "BorderBrush@Normal:=$t",
  "controlStyles[53].styles[5]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[53].styles[6]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[53].styles[7]": "BackgroundSizing=InnerBorderEdge",
  "controlStyles[54].target": "StartDocked.NavigationPaneButton#UserTileButton > Windows.UI.Xaml.Controls.Grid@CommonStates > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[54].styles[0]": "Background@Normal=$t",
  "controlStyles[54].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[54].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[54].styles[3]": "BorderThickness=2",
  "controlStyles[54].styles[4]": "BorderBrush@Normal:=$t",
  "controlStyles[54].styles[5]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[54].styles[6]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[54].styles[7]": "BackgroundSizing=InnerBorderEdge",
  "controlStyles[55].target": "Grid#ContentBorder@CommonStates > Border#BackgroundBorder",
  "controlStyles[55].styles[0]": "Background@Normal=$t",
  "controlStyles[55].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[55].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[55].styles[3]": "BorderThickness=2",
  "controlStyles[55].styles[4]": "BorderBrush@Normal:=$t",
  "controlStyles[55].styles[5]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[55].styles[6]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[55].styles[7]": "BackgroundSizing=InnerBorderEdge",
  "controlStyles[56].target": "StartDocked.PowerOptionsView#PowerButton > StartDocked.NavigationPaneButton#PowerButton > Windows.UI.Xaml.Controls.Grid@CommonStates > Windows.UI.Xaml.Controls.Border#BackgroundBorder",
  "controlStyles[56].styles[0]": "Background@Normal=$t",
  "controlStyles[56].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[56].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[56].styles[3]": "BorderThickness=2",
  "controlStyles[56].styles[4]": "BorderBrush@Normal:=$t",
  "controlStyles[56].styles[5]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[56].styles[6]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[56].styles[7]": "BackgroundSizing=InnerBorderEdge",
  
  "controlStyles[57].target": "Windows.UI.Xaml.Controls.TextBox#ExpandedFolderNameTextBox > Windows.UI.Xaml.Controls.Grid@CommonStates",
  "controlStyles[57].styles[0]": "Background@Normal:=$t",
  "controlStyles[57].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[57].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[57].styles[3]": "Background@Focused:=$t",
  "controlStyles[57].styles[4]": "CornerRadius:=$mcr",
  "controlStyles[57].styles[5]": "BorderThickness=2",
  "controlStyles[57].styles[6]": "BorderBrush@Normal:=$t",
  "controlStyles[57].styles[7]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[57].styles[8]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[57].styles[9]": "BorderBrush@Focused:=$t",
  "controlStyles[57].styles[10]": "BackgroundSizing=InnerBorderEdge",
  "controlStyles[57].styles[11]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",

  "controlStyles[58].target": "Windows.UI.Xaml.Controls.StackPanel#RootPanel > Windows.UI.Xaml.Controls.Button#Header > Windows.UI.Xaml.Controls.Border#Border@CommonStates",
  "controlStyles[58].styles[0]": "Background@Normal=$t",
  "controlStyles[58].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[58].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[58].styles[3]": "BorderThickness=2",
  "controlStyles[58].styles[4]": "BorderBrush@Normal:=$t",
  "controlStyles[58].styles[5]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[58].styles[6]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[58].styles[7]": "BackgroundSizing=InnerBorderEdge",
  "controlStyles[59].target": "Windows.UI.Xaml.Controls.Grid#ContentBorder@CommonStates > Windows.UI.Xaml.Controls.Border#BorderBackground",
  "controlStyles[59].styles[0]": "Background@Normal=$t",
  "controlStyles[59].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[59].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[59].styles[3]": "BorderThickness=2",
  "controlStyles[59].styles[4]": "BorderBrush@Normal:=$t",
  "controlStyles[59].styles[5]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[59].styles[6]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[59].styles[7]": "BackgroundSizing=InnerBorderEdge",

  "controlStyles[60].target": "Windows.UI.Xaml.Controls.ListViewItem > Windows.UI.Xaml.Controls.Grid#ContentBorder@CommonStates > Windows.UI.Xaml.Controls.Border#BorderBackground",
  "controlStyles[60].styles[0]": "Background@Normal=$t",
  "controlStyles[60].styles[1]": "Background@PointerOver:=$nbth",
  "controlStyles[60].styles[2]": "Background@Pressed:=$nbtp",
  "controlStyles[60].styles[3]": "BorderThickness=2",
  "controlStyles[60].styles[4]": "BorderBrush@Normal:=$t",
  "controlStyles[60].styles[5]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[60].styles[6]": "BorderBrush@Pressed:=$nbb",
  "controlStyles[60].styles[7]": "BackgroundSizing=InnerBorderEdge",

  "controlStyles[61].target": "Cortana.UI.Views.CortanaRichSearchBox#SearchTextBox > Windows.UI.Xaml.Controls.Grid@CommonStates > Windows.UI.Xaml.Controls.Border#BorderElement",
  "controlStyles[61].styles[0]": "Background@Focused:=$nbt",
  "controlStyles[61].styles[1]": "Background@Normal:=$nbt",
  "controlStyles[61].styles[2]": "Background@PointerOver:=$nbth",
  "controlStyles[61].styles[3]": "Background@Disabled:=$nbt",
  "controlStyles[61].styles[4]": "BorderThickness=2",
  "controlStyles[61].styles[5]": "BorderBrush@Focused:=$nbb",
  "controlStyles[61].styles[6]": "BorderBrush@Normal:=$nbb",
  "controlStyles[61].styles[7]": "BorderBrush@PointerOver:=$nbb",
  "controlStyles[61].styles[8]": "BorderBrush@Disabled:=$nbb",
  "controlStyles[61].styles[9]": "BackgroundSizing=InnerBorderEdge",
  "controlStyles[61].styles[10]": "BackgroundTransition:=<BrushTransition Duration=\"0:0:0.100\" />",
  
  "controlStyles[62].target": "Windows.UI.Xaml.Controls.Border#TaskbarSearchBackground",
  "controlStyles[62].styles[0]": "Background:=$t",
  "controlStyles[62].styles[1]": "BorderBrush:=$t",
 
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


