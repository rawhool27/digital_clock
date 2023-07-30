# digital_clock

import tkinter as tk
import time

def update_time():
    current_time = time.strftime("%H:%M:%S")
    label.config(text=current_time)
    root.after(1000, update_time)  # Update every 1000ms (1 second)

# Create the main application window
root = tk.Tk()
root.title("Digital Clock")
root.geometry("200x100")

# Create a label to display the time
label = tk.Label(root, font=("Helvetica", 48), fg="black")
label.pack(pady=20)

# Start updating the time
update_time()

# Run the main event loop
root.mainloop()

