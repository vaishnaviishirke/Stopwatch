----------------------------------------------------------------------------------------------------------------
# HMI Stopwatch Project – Omron Sysmac Studio

## Project Overview
This project is a stopwatch application developed using **Omron Sysmac Studio**.
The stopwatch is implemented using structured data types, CPU global variables,
and NA-series HMI screens. The project allows the user to **start, stop, and reset**
the stopwatch and displays time in **hours, minutes, and seconds**.

-----------------------------------------------------------------------------------------------------------------

## Software & Hardware Used
- Omron Sysmac Studio
- Omron NA Series HMI (NA5-7W001-V1)
- Sysmac Studio Version: 1.17

---

## Step-by-Step Project Implementation

### 1. Data Type Creation (CPU Side)
- Navigated to **Data Types** in Sysmac Studio.
- Created a **Structure Data Type** named `Stopwatch`.
- Inside the structure, added the following members:
  - `Hours`
  - `Minutes`
  - `Seconds`
  - `Start`
  - `Stop`
  - `Reset`
- These members define both the time values and control signals for the stopwatch.

📸 
<img width="560" height="190" alt="dt" src="https://github.com/user-attachments/assets/520b7ab1-8f73-4dc4-a87b-2517df628840" />

--------------------------------------------------------------------------------------------------------------------------------------

### 2. CPU Global Variable Creation
- Navigated to **CPU → Global Variables**.
- Created a new global variable named `Stopwatch`.
- Assigned its data type as the previously created **Stopwatch structure**.
- This variable acts as the main interface between the CPU logic and the HMI.

📸 
<img width="593" height="97" alt="gb" src="https://github.com/user-attachments/assets/7fe45d57-1879-47bb-b61a-fd84e8a7804f" />

--------------------------------------------------------------------------------------------------------------------------------------

### 3. Program Creation
- Navigated to **Programs** section.
- Created a new program to handle the stopwatch logic.
- The program processes:
  - Start condition
  - Stop condition
  - Reset condition
  - Time calculation for hours, minutes, and seconds

📸 
<img width="536" height="409" alt="ladder1" src="https://github.com/user-attachments/assets/7f867e2a-24e7-4b99-96a1-002434b02d86" />
<img width="501" height="188" alt="ladder2" src="https://github.com/user-attachments/assets/3ce3ed79-6329-4605-a3eb-cd8a7c18fff1" />

------------------------------------------------------------------------------------------------------------------------------------------

### 4. HMI Configuration
- Inserted a new HMI by selecting:
  - **HMI → Add → NA5-7W001-V1**
  - Version: **1.17**
- Added the HMI to the project.

--------------------------------------------------------------------------------------------------------------------------------------

### 5. HMI Page Design
- Created **two HMI pages**:
  - **Main Page**
  - **Stopwatch Page**
- On the stopwatch page:
  - Added buttons using the **Toolbox**
  - Used **Toggle Buttons** for Start, Stop, and Reset
- Mapped HMI tags to the **same CPU global variables** created earlier.
- Ensured proper tag mapping between HMI and CPU.

📸
<img width="385" height="233" alt="main" src="https://github.com/user-attachments/assets/088e614f-370f-44e0-9aa3-07bc4727a56e" />

📸 
<img width="386" height="233" alt="sw" src="https://github.com/user-attachments/assets/ab342de7-f243-4c88-99be-45ac9519f50b" />

-----------------------------------------------------------------------------------------------------------------------------------------

### 6. Simulation
- Ran the simulation using **Simulation with Controller**.
- Verified stopwatch functionality:
  - Start
  - Stop
  - Reset
- Confirmed correct time calculation and HMI interaction.
-----------------------------------------------------------------------------------------------------------------------------

## Author
**Vaishnavi Shirke**

Industrial Automation | PLC | HMI | Robotics




