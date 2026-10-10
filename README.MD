# Overhaulded Task Switcher
 
A modern, fluid and highly visual replacement for the native Windows Alt+Tab experience.

Built from scratch in native C++ as a project to explore Windows APIs, graphics, animation systems and desktop customization. You can also see the original [GITHUB REPOSITORY](https://github.com/IMiloDev/OverhauldedWin) to send me issues.

> **⚠️ DISCLAIMER**
>
> If the **Windhawk window is in the foreground**, the native Windows Task Switcher may appear above Overhaulded during `Alt + Tab`.
> 
> **Workaround:** Minimize or close the Windhawk window before using Overhaulded.
>
> [Read more about this limitation →](#native-windows-task-switcher)
> 

## Screenshot

![OverhauldedWin Task Switcher](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/TaskManager.jpg)

## Features

* Modern horizontal task switcher interface
* App grouping by application/process
* Real DWM window previews
* Dynamic Obsidian visual system
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
* Smoothest carousel-style navigation
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

---

# IMPORTANT

Overhaulded is still a pre-release project.

Some applications may behave differently than standard desktop windows, especially those using unusual window structures, custom rendering, or multiple processes.

### Native Windows Task Switcher

When the **Windhawk window itself is in the foreground**, Windows keeps the native task switcher on top of Overhaulded when an `Alt + Tab` session is initiated.

In this situation, the native Windows task switcher may appear over the Overhaulded interface, even though Overhaulded uses a "topmost" window and correctly handles keyboard input.

This behavior is related to how the Windows Shell manages its native task switcher and window/composition priority during the `Alt + Tab` operation. Windows does not provide a reliable, documented, and guaranteed public API that allows forcing a third-party window (which does not take focus) to remain visually above the native task switcher.

Behavior may vary depending on the Windows version and system configuration. This is a limitation of the Windows Shell, not a failure to detect or handle `Alt + Tab` input.

I apologize in advance for the inconvenience. I am constantly looking for a way to fix this issue, but public documentation hasn't yielded a solution so far; while it isn't necessarily impossible, it is highly likely that this issue cannot be resolved without delving into sensitive Windows ecosystem code.

---

## Controls

| Shortcut                                     | Action                        |
| -------------------------------------------- | ----------------------------- |
| `Alt + Tab`                                  | Move to the next window       |
| `Alt gr+ Tab`                                | Move to the next window       |
| `Alt + Tab` + release `Alt`                  | Activate the selected window  |
| `Esc`                                        | Cancel the switcher           |
| `Alt gr + Tab + Arrows` `Alt + Tab + Arrows` | Additional navigation/control |

## Compatibility

Overhaulded is currently designed specifically for Windows 11.

The project is still under active development, so behavior may vary depending on:

* Display scaling
* Multiple-monitor configurations
* Windows configuration
* Application window types
* Other Alt+Tab/task-switcher modifications

Running multiple applications that replace the native Windows task switcher at the same time may cause conflicts.

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

See the https://github.com/IMiloDev/OverhauldedWin/blob/main/LICENSE file for the complete license text.

---

> Made by Milo.

![OverhauldedWin Task Switcher](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/preview.gif)
