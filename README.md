# Fullscreen Clock with Alarm

A simple fullscreen digital clock built with Python's `tkinter` module. Apart from just telling the time, the clock also has a basic alarm feature.

## Features:
- **4 Versions**:
  V-1.01: Round clock.
  v-1.02: Round clock with alarm.
  v-1.03: Round clock with GPIO Buzzer alarm.
  v-1.04: Round clock with audio file.
- **Fullscreen Clock**: Display time in a frameless window mode.
- **Interactive**: Click anywhere on the screen to close the application.
- **Set Alarm**: Incremental buttons to set hours and minutes for the alarm.
- **Visual Alarm**: A pop-up notification appears when the alarm rings.

## Prerequisites:
- Python 3.x
- `tkinter` module (typically comes pre-packaged with Python standard distributions).

## Installation:
Clone the repository and navigate to the directory:
```bash
git clone https://github.com/B-Boone/Alarm_Clock
cd Alarm_Clock
```

## How to Use: 
1. **Run the Application**:
  V-1.01
  ```bash
  python3 clock_base.py
  ```
  V-1.02
  ```bash
  python3 alarm_clock_base.py
  ```
  V-1.03
  ```bash
  python3 alarm_clock_gpio.py
  ```
  V-1.03
  ```bash
  python3 alarm_clock_audio.py
  ```

2. **Set the Alarm**: Click the 'Set Hour' and 'Set Minute' buttons to set the alarm.
3. **Exit**: Click anywhere on the clock to exit the program.
4. **Alarm Notification**: A pop-up will appear when the alarm rings. Press the "OK" button to close the notification and stop the alarm.

## Structure:
- **Clock Class**: Inherits from `tk.Tk`.
  - Has methods to draw the clock hands, hour marks, numbers, and check the alarm.
  - Contains button commands to set the alarm hour and minute.
- **cleanup_on_exit**: A function to handle the cleanup process on exit.

## Customization: *Applies to all versions*
- **Colors**: When you want to change the color scheme.
  1. Search for every instance of the mention white.
  2. Paying attention to what each mention of white affects, change to whatever color you'd like
  3. Same applies when changing the background, just search for black instead.
- **Locations**: When you need to adjust the buttons and alarm locations.
  1. EDIT x= and y=:
     ```bash
        # Display for alarm time
        self.alarm_display = tk.Label(self.canvas, text="--:--", font=('Arial', 20, 'bold'), bg="black", fg="white")
        self.alarm_display.place(x=self.screen_width - 10, y=50, anchor="e")

        # Buttons for setting the alarm
        self.hour_button = tk.Button(self.canvas, text="Set Hour", command=self.set_alarm_hour, bg="white", width=10, height=5)
        self.hour_button.place(x=self.screen_width, y=200, anchor="e")

        self.minute_button = tk.Button(self.canvas, text="Set Minute", command=self.set_alarm_minute, bg="white", width=10, height=5)
        self.minute_button.place(x=self.screen_width, y=300, anchor="e")
     ```
- **EXAMPLE**:
  
     ```bash
        # Display for alarm time
        self.alarm_display = tk.Label(self.canvas, text="--:--", font=('Arial', 20, 'bold'), bg="black", fg="purple")
        self.alarm_display.place(x=self.screen_width - 686, y=430, anchor="e")

        # Buttons for setting the alarm             # Added fg=
        self.hour_button = tk.Button(self.canvas, text="Set Hour", command=self.set_alarm_hour, bg="black", fg="purple", width=10, height=5)
        self.hour_button.place(x=self.screen_width -686, y=430, anchor="e")

        self.minute_button = tk.Button(self.canvas, text="Set Minute", command=self.set_alarm_minute, bg="black",  fg="purple", width=10, height=5)
        self.minute_button.place(x=self.screen_width, y=430, anchor="e")
     ```

## Contributing:
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License:
[MIT](https://choosealicense.com/licenses/mit/)

---

ENJOY!
