!pip install matplotlib numpy
import matplotlib.pyplot as plt # import the pyplot module from matplotlib
import numpy as np

# Define ev_bars and gas_bars
# Example: Assuming you have data for EV and Gas cars
ev_data = [30, 21, 40]  # Added data for the fourth category
gas_data = [75, 67, 63] # Added data for the fourth category

# Define x-axis positions for the bars
x_positions = np.arange(len(ev_data))  # [0, 1, 2, 3]

# Width of each bar
bar_width = 0.35

# Create bar plots and store the bar objects in ev_bars and gas_bars, with custom colors
ev_bars = plt.bar(x_positions, ev_data, width=bar_width, label='EV', color='green')  # Change EV bar color to skyblue
gas_bars = plt.bar(x_positions + bar_width, gas_data, width=bar_width, label='Gas', color='black') # Change Gas bar color to coral

# Now you can iterate through the bar objects
for bar in ev_bars + gas_bars:
    yval = bar.get_height()
    plt.text(bar.get_x() + bar.get_width() / 2, yval, round(yval, 1), ha='center', va='bottom')

# Add labels to the x and y axes
plt.xlabel("Fuel Type")  # Replace with your desired x-axis label
plt.ylabel("Lifetime Emissions (metric tons CO2)") # Replace with your desired y-axis label

# Set x-axis tick positions and labels
plt.xticks(x_positions + bar_width / 2, ['United States', 'Europe', 'China']) 

# Set y-axis limits
plt.ylim(0, 100)  # Set the y-axis range from 0 to 100

plt.savefig("lifetime_emissions_comparison.png")
plt.legend()  # Add a legend to differentiate EV and Gas bars
plt.show() # Display the bar plot
