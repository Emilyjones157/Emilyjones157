import math

# Provided data
data = [
    42.40, 32.20, 45.80, 49.80, 42.00, 43.90, 57.90, 48.90, 34.10, 34.40, 30.60, 39.10, 36.50, 48.50, 41.80, 56.60,
    46.80, 53.40, 53.70, 45.10, 38.50, 34.40, 44.70, 38.80, 55.60, 35.10, 41.20, 31.70, 39.40, 53.60, 34.40, 69.20,
    25.20, 44.00, 53.00, 53.00, 46.40, 36.20, 33.10, 40.00, 44.10, 35.20, 44.20, 48.10, 38.00, 24.50, 37.20, 42.20,
    34.20, 41.40, 45.40, 53.50, 51.40, 40.10, 37.30, 30.40, 31.70, 46.70, 39.90, 32.80, 28.40, 38.60, 45.10, 38.90,
    44.00, 46.20, 49.90, 36.50, 38.10, 47.90, 43.40, 37.90, 38.00, 38.80, 48.80, 44.80, 35.80, 45.20, 43.00, 27.50,
    41.80, 41.60, 39.00, 57.30, 42.90, 46.60, 46.90, 37.60, 44.40, 39.10, 24.00, 35.00, 44.60, 54.20, 44.90, 41.50,
    45.10, 39.60, 36.50, 38.30
]

# Step 1: Calculate the Mean
mean_lifetime = sum(data) / len(data)

# Step 2: Calculate the Squared Deviation from the Mean for Each Data Point
squared_deviations = [(x - mean_lifetime) ** 2 for x in data]

# Step 3: Sum the Squared Deviations
sum_squared_deviations = sum(squared_deviations)

# Step 4: Calculate the Variance
variance_lifetime = sum_squared_deviations / len(data)

# Step 5: Calculate the Standard Deviation
std_dev_lifetime = math.sqrt(variance_lifetime)

print(f"The standard deviation is approximately {std_dev_lifetime:.3f}")
