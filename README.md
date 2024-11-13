# Fossil-Fuels-vs.-Electric-Vehicles
Who and what is harmed by the power plants and mining due to fossil fueled vehicles compared to EVs?

# Lifetime CO2 Emissions of Gasoline and Electric Cars (EVs)
pip install matplotlib numpy
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

This graph highlights variations depending on regional energy sources by comparing the lifetime CO2 emissions of gasoline and electric cars (EVs) in the US, Europe, and China. Over their lifetime, EVs in the US release about 30 metric tons of CO₂, which is almost 60% less than that of gasoline-powered vehicles, which emit 75 metric tons. With its vast array of renewable energy sources, Europe exhibits even larger reductions; EVs emit 21 metric tons, compared to 67 for gasoline-powered vehicles, a 69% decrease. In China, where coal is still a significant source of electricity, EVs generate roughly 40 metric tons, a 37% difference from gasoline's 63 metric tons. Similarly, EVs in India emit about 50 metric tons, while gasoline-powered vehicles emit 62 metric tons, a smaller 19% decrease as a result of the significant use of fossil fuels. In general, EVs emit far fewer pollutants than gasoline-powered vehicles, particularly in areas with cleaner electrical grids. This highlights the significance of renewable energy in optimizing the environmental advantages of EVs.

# Environmental Impacts of Nickel Mining
![nickelmining](https://github.com/user-attachments/assets/b368db3b-0280-4649-8116-fb160481a030)

Significant environmental effects have resulted from the growing demand for nickel in electric vehicle (EV) batteries, particularly in Indonesia, which has some of the greatest nickel reserves in the world. In order to make room for mining facilities like the Indonesia Weda Bay Industrial Park (IWIP), forests that are essential for storing carbon are being extensively cleared—more than 5,331 hectares on Halmahera Island alone. In addition to releasing carbon dioxide, this deforestation disturbs ecosystems. In addition, nickel mining operations pollute adjacent rivers, tainting water supplies that are vital to the populations that depend on them. In addition to the coal-fired power plants at IWIP producing 3.78 gigawatts yearly, which further contributes to local air pollution and has an adverse effect on the health of local residents, fishermen in the vicinity complain that filthy water has forced them farther out to sea in search of uncontaminated fish.
