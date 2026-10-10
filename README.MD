# Overhaulded Task Switcher
 
A modern, fluid and highly visual replacement for the native Windows Alt+Tab experience.
 
Built from scratch in native C++ as a project to explore Windows APIs, graphics, animation systems and desktop customization. You can also see the original [GITHUB REPOSITORY](https://github.com/IMiloDev/OverhauldedWin) to send me issues.

> **⚠️ DISCLAIMER**
>
> When an **elevated window** is focused, Windows may not deliver low-level keyboard input to a normal-privilege process (UIPI). Windhawk 2.0's UIAccess tool process is included to handle this case; the Explorer hotkey forwarder remains an experimental fallback.
>
> [Read more about this limitation →](#elevated-window-input)

## Screenshot

![OverhauldedWin Task Switcher](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/task-manager.jpg)

## Features

- Modern horizontal task switcher interface
- App grouping by application/process
- Real DWM window previews
- Dynamic Obsidian visual system
- Rounded cards with subtle downward shadows
- Floating task switcher surface
- Fluid opening animation
- Smooth horizontal navigation
- Interruptible navigation animations
- Subtle center-card snap animation
- Hover interactions
- Window closing
- Resolution-aware UI scaling
- High-DPI support
- Alt + Tab support
- Alt + Shift + Tab support
- AltGr + Tab support
- Lightweight native C++ implementation
- Background execution for fast activation

### Another Features

- Visual continuity between selections
- Smoothest carousel-style navigation
- Real window previews
- Application-aware grouping
- Subtle depth and lighting
- Fast activation through background execution

Overhaulded also aims to remain visually distinct from other Windows task-switcher projects while exploring its own interaction and visual language.

## Design

Overhaulded focuses on a dark, minimal interface inspired by modern desktop UI design while keeping the selector feeling native to Windows.

The visual system uses a Black Obsidian surface with:

- Rounded cards
- Subtle downward shadows
- Content-based illumination
- Soft depth separation
- Smooth transitions
- A fixed central visualizer

The central visualizer remains fixed while the cards move through the carousel, creating the impression of navigating through a physical stack of windows rather than moving the entire interface.

## Smooth Animations

### Open / Close

![OverhauldedWin Open Animation](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/open-close.webp)

### Navigation

![OverhauldedWin](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/desplace.webp)

### Window Close

![OverhauldedWin](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/window-close.webp)

## Background Execution

Overhaulded remains prepared in the background instead of creating the entire task-switcher interface from scratch every time Alt+Tab is pressed.

This allows the selector to appear immediately while keeping the visual opening animation smooth.

The architecture separates global input handling from the UI/rendering system so that heavy graphics and window-management operations do not run directly inside low-level keyboard hooks.

---

# IMPORTANT

Overhaulded is still a pre-release project.

Some applications may behave differently than standard desktop windows, especially those using unusual window structures, custom rendering, or multiple processes.

### Elevated Window Input

A standard-privilege process cannot reliably receive low-level keyboard events while an elevated window is focused because of Windows UIPI. On Windhawk 2.0, this mod includes `windhawk-mod-uiaccess.exe` so the tool process can use UIAccess for this scenario. The Explorer hotkey-forwarding component is retained as an experimental fallback. Behavior can still vary by Windows version and configuration; if Alt+Tab falls back to the native switcher, verify that the UIAccess-capable process is available and enabled.

---

## Controls

| Shortcut                                     | Action                        |
| -------------------------------------------- | ----------------------------- |
| `Alt + Tab`                                  | Move to the next window       |
| `Alt + Shift + Tab`                          | Move to the previous window   |
| `AltGr + Tab`                                | Move to the next window       |
| `Alt + Tab` + release `Alt`                  | Activate the selected window  |
| `Esc`                                        | Cancel the switcher           |
| `Alt + Tab` + arrows                       | Navigate through the selector  |
| `AltGr + Tab` + arrows                      | Navigate through the selector  |

## Compatibility

Overhaulded is currently designed specifically for Windows 11.

The project is still under active development, so behavior may vary depending on:

- Display scaling
- Multiple-monitor configurations
- Windows configuration
- Application window types
- Other Alt+Tab/task-switcher modifications

Running multiple applications that replace the native Windows task switcher at the same time may cause conflicts.

## Development

Overhaulded is primarily a C++ project focused on exploring:

- Win32 APIs
- Windows hooks
- DWM
- Direct2D
- DirectWrite
- GDI
- Window management
- High-DPI rendering
- Desktop animation systems
- Native Windows UI

The project is continuously evolving as new ideas and technical improvements are explored.

## License

This project is licensed under the **MIT License**.

See the https://github.com/IMiloDev/OverhauldedWin/blob/main/LICENSE file for the complete license text.

---

> Made by Milo.

![OverhauldedWin Task Switcher](https://raw.githubusercontent.com/IMiloDev/OverhauldedWin/main/assets/icons/preview.gif)
