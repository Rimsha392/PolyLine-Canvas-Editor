# 🎨 PolyLine Canvas Editor — Phase 1: Requirements Analysis
**Academic Submission:** Rimsha Hussain (Student A)  
**Focus:** Project Initialization & Interface Requirements

---

## 📌 Project Vision & Interaction Design
The primary objective is the architecting of a high-fidelity, responsive, web-based environment for the **manipulation of geometric primitives**. The design prioritizes **modal interaction**, balancing high-precision pointing (Direct Manipulation) with an efficient **Keyboard-Accelerator** system to reduce cognitive load and enhance user throughput.

---

## 📋 1.1 Functional Requirements (Interaction Taxonomy)
As the lead for Phase 1, I have established a robust **Affordance Model** consisting of eight core system interactions:

* **Creation (Modal Entry):** Initialization of new polyline entities via key-trigger (**B**) with asynchronous vertex instantiation via discrete input events.
* **Manipulation (Direct Control):** Support for vertex translation (**M**) and edge-splitting/interpolation (**I**) to modify existing geometry.
* **Deletion (Geometric Pruning):** Heuristic-based removal of the vertex nearest to the cursor (**D**), followed by an automated **Topological Re-connection** to maintain path continuity.
* **Systemic Controls:** * **State Reset:** Canvas clearing via the (**R**) hotkey.
    * **Termination:** Application exit via (**Q**).
    * **Data Persistence:** State serialization/deserialization (JSON) via standard **Command-Key Accords** (**Ctrl+S / Ctrl+O**).

---

## ⚙️ 1.2 System Constraints & Performance Metrics
To ensure an optimal **User Experience (UX)**, the system is bound by the following technical heuristics:

* **Computational Capacity:** The rendering engine must manage a complexity of up to **100 discrete polyline entities** without degradation.
* **Latency Thresholds:** Performance must sustain a **60 FPS** refresh rate, ensuring a **frame budget of $\le 16.67ms$** to prevent "interaction lag" and maintain visual fluidity.
* **UI Philosophy:** A minimalist, **Non-Intrusive Interface** to maximize the user's "Display-to-Action" ratio within the canvas workspace.

---

## 🚩 Challenges and Confusions (HCI Reflection)
* **Version Control Sync (Git):** Encountered a **State Synchronization Conflict** between the local working tree and remote origin. This was mitigated by re-initializing the `.git` architecture to establish a clean individual submission lineage.
* **Vertex "Healing" Heuristics:** A significant design challenge involved calculating the **Euclidean Distance** for vertex selection and ensuring the path re-closed correctly without violating geometric logic during deletions.
* **Input Polling & Refresh Rates:** Analyzing the trade-off between high-frequency mouse polling and the Canvas API's drawing loop to prevent "jank" during the **Insert (I)** preview phase.