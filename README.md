# Fossil-Fuels-vs.-Electric-Vehicles
Who and what is harmed by the power plants and mining due to fossil fueled vehicles compared to EVs?
import matplotlib.pyplot as plt

# Data for environmental impact from nickel mining for EVs, excluding water and air pollution
categories = ['Deforestation (Hectares Cleared)', 
              'Carbon Storage Loss (Tons)']
values = [5331, 7000]  # Example values for deforestation and carbon storage loss

# Create horizontal bar plot
plt.figure(figsize=(8, 4))
bars = plt.barh(categories, values, color=['#8fcbbc', '#125e3c'])

# Add title and labels
plt.xlabel("Impact Level")
plt.title("Environmental Impacts of Nickel Mining for EVs")

# Display value labels on each bar with units
labels = ["5331 Hectares", "7000 Tons"]
for bar, label in zip(bars, labels):
    plt.text(bar.get_width() + 50, bar.get_y() + bar.get_height() / 2, label,
             ha='center', va='center')

# Show the plot
plt.show()
