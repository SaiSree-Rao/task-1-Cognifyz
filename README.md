# task-1-Cognifyz
import pandas as pd

# Loading the dataset
df = pd.read_csv('Dataset.csv')
cuisine_counts = df['cuisines'].value_counts()

# Getting the top three most common cuisines
top_three_cuisines = cuisine_counts.head(3)

# Calculating the total number of restaurants
total_restaurants = len(df)

# Calculating the percentage of restaurants serving each of the top cuisines
percentage_top_cuisines = (top_three_cuisines / total_restaurants) * 100

print("Top three most common cuisines:")
print(top_three_cuisines)

print("\nPercentage of restaurants serving each of the top cuisines:")
print(percentage_top_cuisines)
