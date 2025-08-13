# 🍅 Pomodoro Timer

A simple, yet powerful, command-line Pomodoro timer written in Bash. This script helps you stay focused by cycling through work and break periods, complete with a visual progress bar and notifications.

It's designed to be lightweight, easy to use, and highly customizable right from your terminal.

---

## ✨ Features

* **Custom Intervals:** Easily set your own work and break durations using command-line flags.
* **Endless Loop:** The timer continuously cycles between work and break sessions to keep you in the zone.
* **Manual Control:** Always waits for a key press before starting the next session, so you're always in control.
* **Visual Progress Bar:** Utilizes [`caarlos0/timer`](https://github.com/caarlos0/timer) to display a colorful, real-time progress bar.
* **Rich Notifications:** Get both desktop pop-up notifications and spoken alerts when a session ends.

---

## ⚙️ Prerequisites

Before you begin, ensure you have the following tools installed on your system.

* **[timer](https://github.com/caarlos0/timer):** The core visual timer. Follow the installation instructions on their GitHub page.
* **`spd-say`:** For voice notifications. This is part of the `speech-dispatcher` package.
    ```sh
    sudo apt install speech-dispatcher
    ```

---

## 🚀 Installation

1.  **Clone the repository**
    ```sh
    git clone https://github.com/tomasmach/pomodoro-timer.git
    cd pomodoro-script
    ```

2.  **Make the script executable**
    You need to give the script permission to run.
    ```sh
    chmod +x pomodoro
    ```

3.  **Create a symbolic link**
    To make the `pomodoro` command available system-wide, we'll link it to `~/.local/bin`.
    ```sh
    # Ensure the target directory exists
    mkdir -p ~/.local/bin

    # Create the link
    ln -s "$(pwd)/pomodoro" ~/.local/bin/pomodoro
    ```
    Now you can call `pomodoro` from anywhere!

---

## 💡 Usage

Running the timer is simple.

* **To start with default times (45 min work / 10 min break):**
    ```sh
    pomodoro
    ```

* **To start with custom times (e.g., 25 min work / 5 min break):**
    ```sh
    pomodoro --work 25 --break 5
    ```

Press `Ctrl+C` at any time to exit the timer.
