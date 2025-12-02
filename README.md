def water_intake(weight, activity):
    # Base water requirement: 35 ml per kg
    base_intake = weight * 35  # in ml

    # Additional water based on activity level
    if activity == 1:  # low activity
        extra = 0
    elif activity == 2:  # moderate activity
        extra = 500
    elif activity == 3:  # high activity
        extra = 1000
    else:
        return "Invalid activity level!"

    total_intake_ml = base_intake + extra
    total_intake_liters = total_intake_ml / 1000

    return round(total_intake_liters, 2)


print("---- Water Intake Calculator ----")
weight = float(input("Enter your weight (kg): "))
print("Activity Level: 1) Low  2) Moderate  3) High")
activity = int(input("Choose activity level (1/2/3): "))

result = water_intake(weight, activity)
print("Recommended daily water intake:", result, "liters")

this is a simple python code for how much water intakeby a person according to their weght
