# Typing Ballons (Assembly Game) 🎈

A fully functional Typing Ballons game written in **x86 Assembly Language** using **NASM**. 
This project demonstrates advanced assembly concepts like hardware interrupts (Timer), direct video memory access, and PC speaker sound generation.

**Authors:** 24L-0618 & 24L-0514

## 🎮 Game Description
Letters float up inside balloons from the bottom of the screen. The player must type the corresponding letter on the keyboard to "pop" the balloon before it hits the top.

* **Level 1:** Single balloons.
* **Level 2:** Two balloons appear simultaneously (starts after 30 seconds).
* **Game Over:** If a balloon hits the top limit.

## ⚙️ Key Features
* **Multitasking:** Uses the Timer Interrupt (INT 08h) to update the clock and game state in the background.
* **Sound Effects:** Custom sound generation using Ports 42h, 43h, and 61h.
* **Graphics:** Direct Video Memory access (0xB800) for fast rendering.
* **RNG:** Linear Congruential Generator for random balloon positions and letters.

## 🚀 How to Run
You will need **DOSBox** and **NASM**.

1.  **Clone or Download** this repository.
2.  Open DOSBox and mount your directory:
    ```bash
    mount c c:\path\to\your\folder
    c:
    ```
3.  **Compile** the code:
    ```bash
    nasm game.asm -o game.com -l game.lst
    ```
4.  **Run** the game:
    ```bash
    game.com
    ```

## 🛠️ Controls
* **A-Z Keys:** Type the letter shown on the balloon to pop it.
* **Enter:** Start game / clear instruction screens.
