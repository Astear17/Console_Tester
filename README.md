# Console Tester
The repository to build a program for testing your gamepad (a.k.a game controller)

## ✨ Overview

The **Gamepad Tester** is a simple, single-file web application designed to help users test and visualize the input from a connected game controller (gamepad). It leverages the **Web Gamepad API** to provide real-time feedback on button presses, analog stick positions, and even controller vibration capabilities.

This is a **pure HTML, CSS, and JavaScript** solution contained entirely within a single `index.html` file, making it easy to host and use.

---

## 🚀 Features

* **Plug and Play:** Automatically detects a connected gamepad when the user interacts with the controller (e.g., presses a button).
* **Real-time Button Status:** Visually highlights pressed buttons and displays their precise analog value (for triggers/buttons that support it).
* **Analog Stick Visualization:** Displays the X/Y coordinates of both the Left and Right analog sticks (Axes 0/1 and Axes 2/3) on an interactive canvas, showing a visual "dot" for the current position.
* **Vibration (Rumble) Test:** Includes buttons to test the controller's haptic feedback (rumble) if supported by the device and browser.
* **Controller Identification:** Displays the unique ID string provided by the Gamepad API to identify the connected device.
* **Standard Mapping:** Uses a standard mapping for common buttons (A, B, X, Y, LB, RB, LT, RT, etc.) for easier identification.

---

## 🛠️ How to Set Up and Run

Since this is a single-file application, setup is extremely simple.

1.  **Save the Code:** Copy the entire HTML code into a file named `index.html`.
2.  **Open in Browser:** Double-click the `index.html` file in your file explorer. It will open in your default web browser.

> **Note:** The Web Gamepad API requires user activation, so you must **press a button or move a stick** on your physical controller after opening the page to activate the connection and start the test loop.

---

## 🕹️ How to Use

1.  **Connect Your Controller:** Ensure your gamepad is plugged in or connected via Bluetooth to your computer.
2.  **Activate:** With the `index.html` page open, **press any button** on your controller.
3.  **Check Status:** The main status message will disappear, and the controller's name and test UI will appear.
4.  **Test Buttons:** Press any button, shoulder, or trigger.
    * The corresponding box in the **Buttons** section will highlight in blue and display its value (usually `1.00` for a digital press). Analog triggers will show values between `0.00` and `1.00`.
5.  **Test Analog Sticks:** Move the Left and Right sticks.
    * The visual dot in the respective canvas circle will move, and the numerical **Axis** values will update (ranging from `-1.0000` to `1.0000`).
6.  **Test Vibration:** If the **Vibration (Rumble)** section is visible, use the buttons to test the haptic feedback.

---

## 💻 Tech Stack

* **HTML5:** Structure of the application.
* **CSS3:** Custom styling for a dark-themed, modern interface.
* **Vanilla JavaScript:** Handles all logic, leveraging the `navigator.getGamepads()` and `window.addEventListener("gamepadconnected", ...)` methods of the **Web Gamepad API**.
* **Canvas API:** Used to visually render the position of the analog sticks.
