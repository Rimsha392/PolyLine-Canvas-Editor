# 🎨 PolyLine Editor
**Phase 1: Requirements & Initialization** | Submitted by: Rimsha Hussain (Student A)

### 🔗 Project Links
* **Live Demo:** [PASTE_YOUR_VERCEL_LINK_HERE]
* **Repository:** https://github.com/Rimsha392/PolyLine-Canvas-Editor

---

## 📌 Project Vision (Requirements)
The goal is a responsive, web-based tool for manipulating geometric polylines using high-precision mouse input and efficient keyboard accelerators.

### 1.1 Functional Requirements (The "Verbs")
* **Creation:** Start new polylines (**B**) and add vertices via discrete clicks.
* **Manipulation:** Move existing vertices (**M**) and insert new ones onto edges (**I**).
* **Deletion:** Remove the nearest vertex (**D**) and "heal" the path via topological reconnection.
* **System Controls:** Clear canvas (**R**), Exit (**Q**), and Save/Load (**Ctrl+S / Ctrl+O**).

### 1.2 Constraints
* **Performance:** Must maintain **60 FPS** (under 16ms latency).
* **Capacity:** Support up to **100 polylines**.
* **UI:** Minimalist interface to prioritize the canvas workspace.

---

## 🚀 Getting Started
1. `npm install`
2. `npm run dev`
3. Open [http://localhost:3000](http://localhost:3000)

---

## 🛠️ Features & Shortcuts

| Tool | Key | Description |
| :--- | :--- | :--- |
| **Draw** | **B** | Click to add points. Double-click/Esc to finish. |
| **Close** | **C** | Connect last vertex to first (Requires 3+ points). |
| **Move** | **M** | Drag vertices to reposition in real-time. |
| **Delete** | **D** | Click nearest vertex to remove it. |
| **Insert** | **I** | Click near an edge to split it. |
| **Undo/Redo**| **Ctrl+Z/Y** | Full editing history. |
| **Export** | **E** | Download as **SVG** or **PNG**. |

### Navigation
* **Scroll:** Zoom (centered on cursor).
* **Space + Drag:** Pan canvas.
* **Ctrl + 0:** Reset view.

---

## 📂 Data Format (JSON v2)
```json
{
  "version": 2,
  "polylines": [
    {
      "id": "a1b2c3",
      "points": [{ "x": 100, "y": 200 }],
      "closed": false,
      "color": "#1E293B",
      "lineWidth": 2
    }
  ]
}