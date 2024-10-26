# room-8
: Regression - Predicting ChatGPT Usage
Use a simple regression to predict the ChatGPT usage for next
week based on historical usage data.

This script calculates a simple trend or slope from the historical usage data and uses it to estimate the usage for the next week.


def predict_usage(usage_values):
    # Calculate the difference between the last and first value
    diff = usage_values[-1] - usage_values[0]
    # Calculate the slope
    slope = diff / (len(usage_values) - 1)
    # Predict the next value
    return usage_values[-1] + slope

# Historical data: hours of usage in the past 4 weeks
usage_values = [50, 60, 70, 80]

# Predict usage for next week
next_week_usage = predict_usage(usage_values)

print(f"Predicted ChatGPT usage for next week: {next_week_usage}")
