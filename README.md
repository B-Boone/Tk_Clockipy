# Fullscreen Clock with Alarm

  A simple fullscreen digital clock built with Python's `tkinter` module. Apart from just telling the time, the clock also has a basic alarm feature.

## Features:

  **4 Versions**:
  
    V-1.00: Round clock. Customized for 1920x1080 resolution.


    v-1.10: Round clock with visual alarm. Customized for 1920x1080 resolution.


    v-1.20: Round clock with GPIO Buzzer alarm. Customized for Raspberry Pi with 640x480 resolution.


    v-1.30: Round clock with audio file alarm. Customized for 800x480 resolution.
  
  **Fullscreen Clock**: Display time in a frameless window mode.
  
  **Interactive**: Click anywhere on the screen to close the application.
  
  **Set Alarm**: Incremental buttons to set hours and minutes for the alarm.
  
  **Visual Alarm**: A pop-up notification appears when the alarm rings.
  

## Prerequisites:

  **Python 3.x**

  **tkinter** module (typically comes pre-packaged with Python standard distributions).

## Installation:

  1. **Clone the repository and navigate to the directory**:

  ```
  git clone https://github.com/B-Boone/Alarm_Clock
  cd Alarm_Clock
  ```

  2. **Install dependencies**:

  ```
  pip3 install tkinter
  ```

## How to Use: 

  1. **Run the Application**:
   
    V-1.00
    ```
    python3 clock_V-1.00.py
    ```
  ![2023-09-29-112542_1920x1080_scrot](https://github.com/B-Boone/Alarm_Clock/assets/101531474/4300af78-4376-4d57-8db2-e8a3c194d26f)


    V-1.10
    ```
    python3 clock_V-1.10.py
    ```
  ![2023-09-29-115625_1920x1080_scrot](https://github.com/B-Boone/Alarm_Clock/assets/101531474/065845a4-a0ba-44df-9b39-90639c432f59)


    V-1.20
    ```
    python3 clock_V-1.20.py
    ```
  ![2023-09-29-114654_640x480_scrot](https://github.com/B-Boone/Alarm_Clock/assets/101531474/1a1fb150-cc61-48be-96fe-14b0fbe9dc59)


    V-1.30
    ```
    python3 clock_V-1.30.py
    ```
  ![2023-09-29-115719_800x480_scrot](https://github.com/B-Boone/Alarm_Clock/assets/101531474/3639c7f4-7d92-447a-9ac9-791f3278707e)


  2. **Set the Alarm**: Click the 'Set Hour' and 'Set Minute' buttons to set the alarm.
   
  3. **Alarm Notification**: A pop-up will appear when the alarm rings. Press the "OK" button to close the notification and stop the alarm.
   
  4. **Exit**: Click anywhere on the clock to exit the program.

## Structure:

  **Clock Class**: Inherits from `tk.Tk`.
  
    - Has methods to draw the clock hands, hour marks, numbers, and check the alarm.
    - Contains button commands to set the alarm hour and minute.

  **cleanup_on_exit**: A function to handle the cleanup process on exit.

## Customization: *Applies to all versions*

  **Colors**: When you want to change the color scheme.
  
    1. Search for every instance of the mention white(on base versions) or purple(on gpio or audio versions).
     
    2. Paying attention to what each mention of white or purple affects, change to whatever color you'd like
     
    3. Same applies when changing the background, just search for black instead.
     
  **Locations**: When you need to adjust the buttons and alarm locations.
  
    EDIT x= and y=:
     
     ```
        # Display for alarm time
        self.alarm_display = tk.Label(self.canvas, text="--:--", font=('Arial', 20, 'bold'), bg="black", fg="white")
        self.alarm_display.place(x=self.screen_width - 10, y=50, anchor="e")

        # Buttons for setting the alarm
        self.hour_button = tk.Button(self.canvas, text="Set Hour", command=self.set_alarm_hour, bg="white", width=10, height=5)
        self.hour_button.place(x=self.screen_width, y=200, anchor="e")

        self.minute_button = tk.Button(self.canvas, text="Set Minute", command=self.set_alarm_minute, bg="white", width=10, height=5)
        self.minute_button.place(x=self.screen_width, y=300, anchor="e")
     ```
     
  **EXAMPLE**:
  
     ```
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

  **[MIT](https://choosealicense.com/licenses/mit/)**

---

## *ENJOY!*
