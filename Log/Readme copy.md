# 🌱 Vertical Farm Project "Plan-T" Log

## 📅 18-03-2025: The real construction is getting closer!
- **Team Plantcontainer**: Going to Action to buy paint, brushes, and other supplies.
- **Team Water**: Looking into calibrating the ion sensors.

---

## 📅 15-03-2025: Waiting on Orders & Preparing (Open-Door Day)
With most of our components on the way, and Mr. Coppens working on the full closet, we are:
- Testing sensors, ESPs, and YAML code.
- Searching for additional materials: white paint, paintbrushes, coconut fiber, etc.

---

## 📅 11-03-2025: PCBs Ordered! 🎉
The PCBs have been ordered from **PCBWay**.

---

## 📅 06-03-2025: First Seeds Sown! 🌱
We sowed our first seeds to be used as a reference, or maybe even to repot them into our working vertical farm soon! 
### 🌿 Planted:
- Basil
- Coriander
- Mint
- Oregano
- Leaf Lettuce

Additionally, we **broke down the old construction**.

---

## 📅 25-02-2025: First Order Placed! 🛒
We ordered several components necessary for our construction. 
### 📦 Sites used:
- Mouser
- TinyTronics
- AliExpress
- PCBWay
- RS

---

## 📅 First Month of Semester 2: Preparation Begins
Each group (Team Plantcontainer, Team Light, Team Water) started researching and designing their part of the system. 
- We **reused as many components as possible** from the old construction.

---

## 📅 17-12-2024: Presentation & Feedback
We presented our progress and collected feedback in our **ClickUp notes**.

---

## 📅 19-11-2024: Planning Phase 📝
While waiting for our **PCBs to arrive**, we:
- Created a schedule.
- Divided the assignment into smaller tasks.
- Assigned tasks to team members.

---

## 📅 22-10-2024: Working on the Old System ⚙️
We gathered to **restart and analyze** the previous system.

### 🔌 Powering Up the System
Using [this guide](https://verticalfarmib3.github.io/inhoud/operation/), we turned everything on:
- **ESPHome server** runs on `192.168.0.40:8123` on the CM3 network.
- **Grafana interface** is accessible via port `3000`.
- **Lights, pumps, fans, and mixer** tested successfully.
- **Automation setup** ensures lights turn on/off at the correct times.

### 📦 Moving the Setup to a New Location
1. Removed the **wood enclosure**.
2. Disassembled the **top and front glass panel**.
3. Cleaned the **old plants and interior**.
4. Moved the **wooden frame**.
5. Installed the **aluminum frame**.

### 🌱 A New Seed
We planted fresh seeds:
- Basil
- Dill
- Chives
- Oregano
- Parsley
- African Marigolds

📌 **Updated light timing**: **08:00 - 20:00**
📌 **Fan schedule**: **5 minutes every 30 minutes**

### ❌ Issues Found
- ⚠️ Mixer only works for **a few seconds** at a time.
- ⚠️ **Drainage tubes clog** due to rockwool.
- ⚠️ **Hot glue was used** instead of waterproof silicone.
- ⚠️ **High startup current** causes relays to melt shut.
- ⚠️ **Faulty moisture sensors** lead to overwatering and leaks.

---

## 📅 16-10-2024: Brainstorming 💡
### 🔄 Fixing the Old System
- **Replace drainage tubes**.
- **Upgrade relays** to better ones.
- **Test alternative substrates** instead of rockwool.
- **Improve water replacement access**.

### 🏡 New System: Modularity Focus
We aim to **design a home-friendly vertical farm**, not an industrial one. Our system should be **modular**:
- **Drawer-based system** inside another drawer.
- **Sensors connected via I2C bus**.
- **Common power rail** for all modules.
- **Plug & Play system** for easy setup.

### 📅 Next Session Goals
- Get the old system running again.

---

## 📸 Concept Drawings
<div style="display: flex; gap: 10px;">
  <img src="./figure1.jpg" alt="Concept 1" width="200"/>
  <img src="./figure2.jpg" alt="Concept 2" width="200"/>
  <img src="./figure3.jpg" alt="Concept 3" width="200"/>
</div>
