# Overhaulded Task Switcher

A modern, fluid and highly visual replacement for the native Windows Alt+Tab experience.

Built from scratch in native C++ as a project to explore Windows APIs, graphics, animation systems and desktop customization. 

> Ofc, made as a C++ practice project. Hope you enjoy it as much as I enjoy developing it.
 
## Screenshot

![OverhauldedWin Task Switcher](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/TaskManager.jpg)

## Features

* Modern horizontal task switcher interface
* App grouping by application/process
* Real DWM window previews
* Dynamic Obsidian visual system
* CPU-based desktop blur
* Rounded cards with subtle downward shadows
* Floating task switcher surface
* Fluid opening animation
* Smooth horizontal navigation
* Interruptible navigation animations
* Subtle center-card snap animation
* Hover interactions
* Window closing
* Resolution-aware UI scaling
* High-DPI support
* Alt + Tab support
* Alt + Shift + Tab support
* AltGr + Tab support
* Lightweight native C++ implementation
* Background execution for fast activation

### Another Features

* Visual continuity between selections
* Smooth carousel-style navigation 
* Real window previews
* Application-aware grouping
* Subtle depth and lighting
* Fast activation through background execution

Overhaulded also aims to remain visually distinct from other Windows task-switcher projects while exploring its own interaction and visual language.

## Design

Overhaulded focuses on a dark, minimal interface inspired by modern desktop UI design while keeping the selector feeling native to Windows.

The visual system uses a Black Obsidian surface with:

* Rounded cards
* Subtle downward shadows
* Content-based illumination
* Soft depth separation
* Smooth transitions
* A fixed central visualizer

The central visualizer remains fixed while the cards move through the carousel, creating the impression of navigating through a physical stack of windows rather than moving the entire interface.

## Smooth Animations

### Open / Close

![OverhauldedWin Open Animation](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/Open_n'_Close.webp)

### Navigation

![OverhauldedWin](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/Desplacement.webp)

### Window Close

![OverhauldedWin](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/abort.webp)

## Background Execution

Overhaulded remains prepared in the background instead of creating the entire task-switcher interface from scratch every time Alt+Tab is pressed.

This allows the selector to appear immediately while keeping the visual opening animation smooth.

The architecture separates global input handling from the UI/rendering system so that heavy graphics and window-management operations do not run directly inside low-level keyboard hooks.

## Requirements

* Windows 11 only
* Windhawk

## Controls

| Shortcut                                         | Action                        |
| ------------------------------------------------ | ----------------------------- |
| `Alt + Tab`                                      | Move to the next window       |
| `Alt gr+ Tab`                                    | Move to the previous window   |
| `Alt + Tab` + release `Alt`                      | Activate the selected window  |
| `Esc`                                            | Cancel the switcher           |
| `Alt gr + Tab + Arrows` `Alt + Arrows`           | Additional navigation/control |

## Compatibility

Overhaulded is currently designed specifically for Windows 11.

The project is still under active development, so behavior may vary depending on:

* Display scaling
* Multiple-monitor configurations
* Windows configuration
* Application window types
* Other Alt+Tab/task-switcher modifications

Running multiple applications that replace the native Windows task switcher at the same time may cause conflicts.

## Known Limitations

Overhaulded is still a pre-release project.

Some applications may behave differently from standard desktop windows, particularly applications that use unusual window structures, custom rendering or multiple processes.

Additional compatibility improvements are planned as development continues.

## Development

Overhaulded is primarily a C++ project focused on exploring:

* Win32 APIs
* Windows hooks
* DWM
* Direct2D
* DirectWrite
* GDI
* Window management
* High-DPI rendering
* Desktop animation systems
* Native Windows UI

The project is continuously evolving as new ideas and technical improvements are explored.

## License

This project is licensed under the **MIT License**.

See the [LICENSE](https://github.com/IMiloDev/OverhauldedWin/blob/main/LICENSE) file for the complete license text.

---
**Overhaulded Task Switcher**
Github [Repo](https://github.com/IMiloDev/OverhauldedWin)
Native C++ • Windows 11 • Windhawk
Made by Milo.
