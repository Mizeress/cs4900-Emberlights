# User Flows & Wireframes Drafts

## Figma Link
https://www.figma.com/design/IT5hoiuID1EiN1TXLCzxiM/Wireframes?node-id=0-1&m=dev&t=xfExrs8XEtBfoII5-1

## User Flow
<img width="581" height="349" alt="Captura de pantalla 2026-09-09 a las 21 33 26" src="https://github.com/user-attachments/assets/8554c638-91f2-43d9-8c8d-9d68eba30727" />


## Wireframes

### View Playlist & Edit
<img width="468" height="352" alt="Captura de pantalla 2026-09-13 a las 19 51 41" src="https://github.com/user-attachments/assets/5aac9ac0-9c51-4156-812e-e09a34299aa4" />



*Note: Users view playlist details and layout. Users can select as many songs as they want to replace, and then another screen will pop up just to confirm that action. Users can also search the song they want to replace.*

### Confirmation
<img width="465" height="353" alt="Captura de pantalla 2026-09-13 a las 19 51 48" src="https://github.com/user-attachments/assets/03ad0f5c-8a01-46db-853f-9315f8ff3df8" />


*Note: Users have to confirm if they want to replace those songs or not.*



## Section: View Playlist & Song Replacement — Heuristic Evaluation & Revisions

## Figma Link
https://www.figma.com/design/cGXDYMt8Bkx89MNN7NlVhh/Second-Version?node-id=30-92&m=dev

### 1. Overview
This section focuses on the **View Playlist** screen and the **Song Replacement** workflow. Following Nielsen's 10 Usability Heuristics, three key usability issues were identified in the initial draft and resolved in the revised wireframes (Second version).

---

### 2. Revised Wireframes (Second version)
<img width="366" height="276" alt="Captura de pantalla 2026-09-13 a las 19 32 28" src="https://github.com/user-attachments/assets/b6ae579b-972e-447c-8243-86a6c20e923c" />

<img width="363" height="273" alt="Captura de pantalla 2026-09-13 a las 19 32 42" src="https://github.com/user-attachments/assets/9a1cab8c-c4e5-480b-87d3-d1fdb67eefba" />

---

### 3. Identified Usability Issues and Applied Fixes

#### Issue 1: Lack of Visual Feedback for Selected Songs
* **Heuristic Name:** Visibility of System Status (Heuristic #1)[cite: 1]
* **Problem Identified:** In the first draft, selecting tracks via checkboxes provided no dynamic feedback near the primary action button, making it unclear how many songs were selected.
* **Fix Applied in V2:** Updated the primary action button to display a dynamic selection counter (`Replace Selected (2)`) and highlighted checked rows in the track table to give immediate visual feedback.

#### Issue 2: Ambiguous Confirmation Prompt 
* **Heuristic Name:** Error Prevention (Heuristic #5) & Recognition Rather Than Recall (Heuristic #6) & Consistency and Standards (Heuristic #4)[cite: 1]
* **Problem Identified:** The original modal used generic text ("Confirmation: YES / NO") with uniform buttons, creating potential confusion and risk of accidental replacement.
* **Fix Applied in V2:** Updated the prompt to explicitly state the action details (`Are you sure you want to replace the selected songs?`). Replaced generic `YES / NO` labels with explicit action buttons (`Confirm` and `Cancel`), applying a distinct primary accent color to the confirmation button for visual hierarchy.

#### Issue 3: Inability to Undo an Accidental Replacement
* **Heuristic Name:** User Control and Freedom (Heuristic #3)[cite: 1]
* **Problem Identified:** Once confirmed, there was no immediate way to reverse an accidental song replacement without manually searching and editing again.
* **Fix Applied in V2:** Implemented a temporary toast notification banner (`Undo (2)`) at the bottom of the view after confirmation, providing a one-click undo option.

  
