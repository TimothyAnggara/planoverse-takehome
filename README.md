# 🛒 Mini 3D Store Layout Prototype

An interactive Unity WebGL prototype that simulates store layout planning. Users can place, move, rotate, and delete store objects like shelves, fridges, and checkouts using an intuitive UI and ghost preview system.

## 🎮 Controls

| Action                            | Input            |
|-----------------------------------|------------------|
| Move camera                       | `W`, `A`, `S`, `D`, `Space` |
| Select Shelf                      | `E` (press again to deselect) |
| Select Fridge                     | `R` (press again to deselect) |
| Select Checkout                   | `T` (press again to deselect) |
| Place object                      | Left Click       |
| Select existing object to move    | Right Click      |
| Rotate ghost                      | Scroll Wheel     |
| Delete selected object            | `Delete`         |

## 🚧 Interaction Behavior

- **Ghost Mode for Placement**: Pressing a hotkey (E/R/T) spawns a translucent ghost version of the object for preview and placement.
- **One Mode at a Time**:  
  - You **cannot select** existing objects while placing a new one.  
  - You **can initiate new placement** while an object is selected — doing so will **put down the selected object** and switch to the new prefab.
- **Deselection**: Pressing the same hotkey twice cancels the ghost and clears selection.
- **Stacking Allowed**: No collision or snapping is currently enforced, so objects can overlap freely.

## ✅ Features Implemented

- Flat floor with raycast-based click-to-place system.
- Live ghost preview with adjustable Y-axis rotation.
- UI key hint display and live selected object text.
- Object selection with right-click and repositioning.
- Object deletion with `Delete` key.
- Modular code structure for prefab management and selection logic.

## 🛠️ Setup

- **Unity Version**: `2022.3.x LTS` recommended.
- Attach the `ObjectPlacement` script to a manager GameObject.
- Assign:
  - `playerCamera` (usually the main camera),
  - `instructionText` (a `TextMeshProUGUI` element),
  - `placeableItems` list (custom prefab-hotkey pairs).

## 📌 To Add Next

- Collision detection and object snapping.
- Grid-based placement and alignment.
- Undo/redo system for layout tweaks.
- Highlight effects when selecting or hovering over objects.
