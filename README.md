
# Flutter SMenus

A Flutter package for dropdown menus, many types of side menus, three dot menus, and popup menus.

<!--
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.
For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/guides/libraries/writing-package-pages).
For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-library-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/developing-packages).
-->

TODO: Put a short description of the package here that helps potential users know whether this package might be useful for them.

# Features

TODO: List what your package can do. Maybe include images, gifs, or videos.
  
## Menus:

|Name                 | Description                                                                                        |
|---------------------|----------------------------------------------------------------------------------------------------|
|SResiableMenu        |A menu that can be resized programatically or phsyically                                            |
|SSlideMenu           |A menu that either slides in, slides in while body slides away, or body slides away to reveal menu  |
|SDropdownMenuCascade |Classic dropdown menu [WIP]                                                                         |
|SDropdownMenuMorph   |Dropdown popup menu using Hero [WIP]                                                                |

# Getting started

## Install

Visit the Install tab for more information

Add this line to your pubspec.yaml

```yaml
dependencies:
    flutter_smenus: ^1.0.0
```

or run this in your project's terminal

```shell
$ flutter pub add flutter_smenus
```

> Remember to run ```flutter pub get```

TODO: List prerequisites and provide or point to information on how to start using the package.

# Showcase


# Code

TODO: Include short and useful examples for package users. Add longer examples to `/example` folder.

Jump to:

SResizableMenu

SResizableMenuNoWrapper

SSlideMenu

SMenuItemButton

SMenuItemCustom

SMenuController

SMenuState

SMenuPosition

SMenuStyle

SMenuItemStyle

SBaseMenu

SBaseMenuState

Custom Menu Items and Menu Builder


## SResizableMenu

```dart
const SResizableMenu({
    super.key,
    this.menuKey,
    this.style,
    this.controller,
    this.items,
    this.builder,
    this.body,
    this.header,
    this.footer,
    this.scrollPhysics,
    this.direction,
    this.duration,
    this.position,
    this.enableSelector,
    this.resizable,
    this.barColor,
    this.barHoverColor,
    this.barSize,
    this.barHoverSize,
  })
```

Sample

```dart
SResizableMenu(
    controller: SMenuController(),
    position: SMenuPosition.left,
    items: [],
    body: Container(),
)
```

<details title=''>
<summary>Parameters</summary>

Either ```items``` or ```builder``` must not be null

|Parameter             |Object Type                           |Default                          |Description |
|----------------------|--------------------------------------|---------------------------------|------------|
|```style```           |SMenuStyle?                           |SMenuStyle()                     |            |
|```controller```      |SMenuController?                      |SMenuController()                |            |
|```items```           |List< SMenuItem>?                     |null                             |            |
|```builder```         |Widget Function(BuildContext context)?|null                             |            |
|```body```            |Widget?                               |Container()                      |            |
|```header```          |Widget?                               |null                             |            |
|```footer```          |Widget?                               |null                             |            |
|```scrollPhysics```   |ScrollPhysics?                        |null                             |            |
|```direction```       |Axis?                                 |Axis.vertical                    |            |
|```duration```        |Duration?                             |const Duration(milliseconds: 250)|            |
|```position```        |SMenuPosition?                        |SMenuPosition.left               |            |
|```enableSelector```  |bool?                                 |false                            |            |
|```resizable```       |bool?                                 |true                             |            |
|```barColor```        |Color?                                |null                             |            |
|```barHoverColor```   |Color?                                |null                             |            |
|```barSize```         |double?                               |3                                |            |
|```barHoverSize```    |double?                               |5                                |            |


</details>

## SResizableMenuNoWrapper

```dart
const SResizableMenuNoWrapper({
    super.key,
    super.style,
    super.controller,
    super.items,
    super.builder,
    super.header,
    super.footer,
    super.scrollPhysics,
    super.direction,
    super.duration,
    super.position,
    this.enableSelector = false,
    this.resizable = true,
    this.barColor,
    this.barHoverColor,
    this.barSize,
    this.barHoverSize,
    })
```

Sample

```dart
Row(
    children: [
        SResizableMenuNoWrapper(
            controller: SMenuController(),
            position: SMenuPosition.left,
            items: [],
        ),
        Expanded(child: Container()),
    ],
)
```

## SSlideMenu

```dart
const SSlideMenu({
    super.key,
    super.style,
    super.controller,
    super.items,
    super.builder,
    super.header,
    super.footer,
    super.scrollPhysics,
    super.direction,
    super.duration,
    super.position,
    this.body,
    this.enableSelector = false,
    this.barrierColor,
    this.enableGestures,
    this.isBodyMovable = true,
    this.isMenuMovable = true
    })
```

Sample

```dart
SSlideMenu(
    controller: SMenuController(),
    position: SMenuPosition.left,
    items: [],
    isBodyMovable = false,
    body: Container(),
)
```
## SDropdownMenuCascade
## SDropdownMenuMorph

## SMenuItemButton
## SMenuItemCustom
## SMenuItemDropdown
## SMenuItemDropdownSelectable

## SMenuStyle
## SDropdownMenuStyle
## SMenuItemStyle

## SMenuPosition
## SDropdownMenuAlignment
## SMenuController
## SMenuState

## SBaseMenu
## SBaseMenuState
## SDropdownMenu
## SDropdownMenuState

## Custom Menu Items and Menu Builder

All menus support custom children.

For items:

```dart
child = <Widget>

builder = (context, style, child) {
    return <Widget>
}
```

or for menus:

```dart
items = <SMenuItem>[];

builder = (context) {
    return <Widget>
}
```

## Upcoming

```dart
const SDropdownMenuCascade
const SDropdownMenuMorph

const SMenuItemDropdown
const SMenuItemDropdownSelectable

const SDropdownMenuAlignment
const SDropdownMenuStyle

const SDropdownMenu
const SDropdownMenuState
```

> Note: Some features may not work with custom children

## Additional information

TODO: Tell users more about the package: where to find more information, how to contribute to the package, how to file issues, what response they can expect from the package authors, and more.