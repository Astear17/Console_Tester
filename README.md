# 🎮 Console Tester

**Console Tester** is a simple, browser-based utility designed to instantly **test and visualize** the input from any connected gamepad (joystick, controller, etc.) using the Web Gamepad API.

It's an essential tool for **developers** checking browser compatibility, or **gamers** verifying if their controller's buttons, analog sticks, and rumble functionality are working correctly before starting a game.

---

## 🚀 Live Demo

The tester is available on https://astear17.github.io/Console_Tester or [clone it and run locally on your device](https://github.com/Astear17/Console_Tester/main/blob/README.md#how-to-clonerun-locally)

---

## ✨ Features

The application provides a real-time, interactive display for key controller inputs:

* **Controller Information:** Displays the connected gamepad's name and ID.

* **Button Testing:** Shows the **pressed state** and **analog value** (from $0.00$ to $1.00$) for every button, including analog triggers.

* **Analog Stick Visualization:** Renders interactive canvases that show the **real-time position** of the Left and Right analog sticks, including their raw **Axis values** (from $-1.0000$ to $1.0000$).

* **Vibration (Rumble) Test:** Allows you to test the controller's rumble feature with short, continuous, and stop functions (requires browser support).

---

## 🛠️ How It Works (Under the Hood)

This project is built as a single-page web application (`index.html`) leveraging modern web standards to provide a high-frequency input check:
| **Component** | **Technology** | **Description** | 
| :--- | :--- | :--- | 
| **Core Functionality** | **JavaScript (Web Gamepad API)** | Uses `navigator.getGamepads()` and `requestAnimationFrame` to poll the controller's state at a high frequency, ensuring minimal input latency. | 
| **Visuals (Sticks)** | **HTML Canvas API** | The analog stick movement is rendered dynamically using the Canvas API to create a visual, central representation of the X/Y axes and the stick's position. | 
| **Structure & Style** | **HTML5 / CSS3** | Provides the structure and a clean, dark-themed, and responsive user interface. | 

## How To Clone/Run Locally

> To follow this tutorial, you must have the **Git** version control system installed on your computer.

### 🚀 Step 1: Clone the Repository
1.  **Open your Bash Terminal** (or Git Bash/Command Prompt if you are on Windows).
2.  **Navigate to the folder** where you want to keep your projects. For example, to go to a 'Projects' folder on your desktop:
    ```bash
    cd ~/Desktop/Projects
    ```
3.  **Execute the `git clone` command.** This downloads all files and the history of the repository and creates a local folder named `Console_Tester`.
    ```bash
    git clone [https://github.com/Astear17/Console_Tester.git](https://github.com/Astear17/Console_Tester.git)
    ```
4.  **Move into the new project directory:**
    ```bash
    cd Console_Tester
    ```
---

### ▶️ Step 2: Running the Project Locally
The project is a single `index.html` file, so no web server is needed!
1.  From inside the `Console_Tester` directory in your terminal, use a command to open the file in your default browser:
    * **On macOS:**
        ```bash
        open index.html
        ```
    * **On Windows (using `start` in Git Bash):**
        ```bash
        start index.html
        ```
    * **On Linux:**
        ```bash
        xdg-open index.html
        ```
