import tkinter as tk
import random

def roll_dice():
    """Function to simulate a dice roll and display the result."""
    dice_result = random.randint(1, 6)
    result_label.config(text=f"You rolled: {dice_result}")

# Create the main window
root = tk.Tk()
root.title("Dice Rolling Simulator")
root.geometry("300x200")

# Create and place a label for the title
title_label = tk.Label(root, text="Dice Rolling Simulator", font=("Helvetica", 16))
title_label.pack(pady=10)

# Create and place a label for the result
result_label = tk.Label(root, text="Click the button to roll the dice", font=("Helvetica", 14))
result_label.pack(pady=20)

# Create and place a button to roll the dice
roll_button = tk.Button(root, text="Roll Dice", font=("Helvetica", 12), command=roll_dice)
roll_button.pack(pady=10)

# Run the application
root.mainloop()
