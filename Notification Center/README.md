# Luminosity theme for Windows 11 Notification Center Styler

**Author**: [mendes.image](https://github.com/mendesimage)

![Demonstration](nc.png)

## Intro
**Luminosity** is based on native Acrylic, using the maximum **TintLuminosityOpacity** value as its backdrop.

It's meant to be used with **Mica** or **MicaAlt** backdrops, with or without the **Translucent Windows** mod.

---

![MediaControlCenter](mediacontrolcenter.png)

---

## General Information

The theme changes the following elements:

- Control and Notification Center
- Notification Pop-Up
- App Group Backdrops
- Rounded several buttons
- Jump Lists
- Context menus

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
  - mbg=<WindhawkBlur BlurAmount="30" TintColor="{ThemeResource CardStrokeColorDefaultSolid}" TintOpacity="0.0" TintLuminosityOpacity="1.0" TintSaturation="1.0" NoiseDensity="1.0" NoiseOpacity="0.1" />
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
  - target: Grid#NotificationCenterGrid
    styles:
      - Background:=$mbg
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: Grid#NotificationCenterTopBanner
    styles:
      - CornerRadius=$wcr
      - Margin=5,6,5,0
  - target: Windows.UI.Xaml.Controls.Grid#RootGrid > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter
    styles:
      - CornerRadius=18
      - Margin=0,0,0,0
  - target: Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#ItemOpaquePlating
    styles:
      - CornerRadius=$mcr
      - BorderBrush:=$t
      - Shadow:=
  - target: Grid#CalendarCenterGrid
    styles:
      - Background:=$mbg
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: ScrollViewer#CalendarControlScrollViewer
    styles:
      - Background:=$t
      - BorderBrush:=$t
  - target: Border#CalendarHeaderMinimizedOverlay
    styles:
      - Background:=$t
  - target: ActionCenter.FocusSessionControl#FocusSessionControl > Grid#FocusGrid
    styles:
      - Background:=$t
      - BorderBrush:=$t
  - target: Windows.UI.Xaml.Controls.Grid#ControlCenterRegion
    styles:
      - Background:=$mbg
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: ScrollViewer#ListContent
    styles:
      - Background:=$t
      - BorderBrush:=$t
  - target: Windows.UI.Xaml.Controls.Grid#L1Grid > Border
    styles:
      - Background:=$t
      - BorderBrush:=$t
  - target: Windows.UI.Xaml.Controls.ContentPresenter
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb > Windows.UI.Xaml.Controls.Border
    styles:
      - Background:= <AcrylicBrush TintColor="{ThemeResource CardStrokeColorDefaultSolid}" FallbackColor="{ThemeResource CardStrokeColorDefaultSolid}" TintOpacity="0.5" TintLuminosityOpacity="1.0" Opacity="1"/>
  - target: Grid#MediaTransportControlsRegion
    styles:
      - Background:=$mbg
      - CornerRadius=$wcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Height=470
      - Shadow:=
  - target: Windows.UI.Xaml.Controls.Grid#MediaTransportControlsRegion
    styles:
      - Height=470
  - target: Windows.UI.Xaml.Controls.Grid#AlbumTextAndArtContainer
    styles:
      - Height=347
  - target: Windows.UI.Xaml.Controls.Grid#ThumbnailImage
    styles:
      - Width=300
      - Height=300
      - HorizontalAlignment=Center
      - VerticalAlignment=Top
      - Grid.Column=1
      - Margin=0,2,0,0
  - target: Windows.UI.Xaml.Controls.Grid#ThumbnailImage > Windows.UI.Xaml.Controls.Border
    styles:
      - CornerRadius=10
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer
    styles:
      - VerticalAlignment=Bottom
      - Grid.Column=0
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer > Windows.UI.Xaml.Controls.TextBlock#TitleText
    styles:
      - TextAlignment=Center
  - target: Windows.UI.Xaml.Controls.StackPanel#PrimaryAndSecondaryTextContainer > Windows.UI.Xaml.Controls.TextBlock#SubtitleText
    styles:
      - TextAlignment=Center
  - target: Grid#MediaTransportControlsRoot
    styles:
      - Background:=<SolidColorBrush Color="Transparent"/>
  - target: MenuFlyoutPresenter
    styles:
      - CornerRadius:=$mcr
      - BorderThickness:=$bt
      - BorderBrush:=$bb
      - Shadow:=
  - target: Border#JumpListRestyledAcrylic
    styles:
      - Background:=$mbg
      - CornerRadius:=$mcr
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: Border#ToastBackgroundBorder2
    styles:
      - Background:=$mbg
      - CornerRadius=$wcr
      - Shadow:=
  - target: Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot
    styles:
      - Background:=$mbg
      - CornerRadius=13
      - BorderThickness=$bt
      - BorderBrush=$bb
      - Shadow:=
  - target: Windows.UI.Xaml.Controls.Grid#FooterGrid
    styles:
      - BorderBrush:=$t
  - target: ActionCenter.MultiLineTextBox#Edit
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.MenuFlyoutItem
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.MenuFlyoutSubItem
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.ListViewItem
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.ContentPresenter#PageHeader
    styles:
      - Background:=$t
  - target: Windows.UI.Xaml.Controls.ContentPresenter > Windows.UI.Xaml.Controls.Border
    styles:
      - BorderBrush:=$t
  - target: Windows.UI.Xaml.Controls.Primitives.ListViewItemPresenter#Root > Border
    styles:
      - CornerRadius=$bcr
  - target: Windows.UI.Xaml.Controls.Primitives.RepeatButton#PreviousButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter@CommonStates
    styles:
      - Background@Normal:=$mbt
      - Background@PointerOver:=$mbth
      - Background@Pressed:=$mbtp
      - RenderTransform:=<TranslateTransform X="15" Y="0" />
      - BorderBrush=$bbb
      - BorderThickness@Normal=$bt
      - BorderThickness@PointerOver=$bt
      - BorderThickness@Pressed=$bt
  - target: Windows.UI.Xaml.Controls.Button#PlayPauseButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter@CommonStates
    styles:
      - Background@Normal:=$mbt
      - Background@PointerOver:=$mbth
      - Background@Pressed:=$mbtp
      - Width=110
      - BorderBrush=$bbb
      - BorderThickness@Normal=$bt
      - BorderThickness@PointerOver=$bt
      - BorderThickness@Pressed=$bt
  - target: Windows.UI.Xaml.Controls.Primitives.RepeatButton#NextButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter@CommonStates
    styles:
      - Background@Normal:=$mbt
      - Background@PointerOver:=$mbth
      - Background@Pressed:=$mbtp
      - RenderTransform:=<TranslateTransform X="-15" Y="0" />
      - BorderBrush=$bbb
      - BorderThickness@Normal=$bt
      - BorderThickness@PointerOver=$bt
      - BorderThickness@Pressed=$bt
  - target: Windows.UI.Xaml.Shapes.Rectangle#HorizontalTrackRect
    styles:
      - Fill:=$bbb
  - target: MenuFlyoutPresenter > Border
    styles:
      - Background:=$mbg
  - target: ScrollViewer#MenuFlyoutPresenterScrollViewer > Border > Grid > ScrollContentPresenter > ItemsPresenter > StackPanel
    styles:
      - ChildrenTransitions:=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled="True" FromHorizontalOffset="-50" FromVerticalOffset="50" /></TransitionCollection>
  - target: Windows.UI.Xaml..Controls.Grid#JumpListGrid > Windows.UI.Xaml.Controls.Grid#SystemItemsContainer > Windows.UI.Xaml.Controls.Border > JumpViewUI.SystemItemListView#SystemItemList > Windows.UI.Xaml.Controls.StackPanel
    styles:
      - ChildrenTransitions:=<TransitionCollection><EntranceThemeTransition IsStaggeringEnabled="True" FromHorizontalOffset="-50" FromVerticalOffset="50" /></TransitionCollection>
  - target: Grid#LayoutRoot
    styles:
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.100" />
  - target: Border#BackgroundBorder
    styles:
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.100" />
  - target: Border#BackgroundBorder
    styles:
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.100" />
  - target: Border#BackgroundBorder
    styles:
      - BackgroundTransition:=<BrushTransition Duration="0:0:0.100" />
  - target: Windows.UI.Xaml.Controls.Grid#FocusGrid
    styles:
      - Background:=$t
      - BorderBrush:=$t
  - target: ControlCenter.ControlCenterView#ControlCenterView > Windows.UI.Xaml.Controls.Grid#RootGrid > Windows.UI.Xaml.Controls.Border#RootGridBorder > Windows.UI.Xaml.Controls.Grid#L1Grid > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.ContentControl#TogglesGroup > Windows.UI.Xaml.Controls.ContentPresenter > ControlCenter.PaginatedGridView > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.GridView#RootGridView > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.ScrollViewer#ScrollViewer > Windows.UI.Xaml.Controls.Border#Root > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.ScrollContentPresenter#ScrollContentPresenter > Windows.UI.Xaml.Controls.ItemsPresenter
    styles:
      - Height=50
```
</details>
