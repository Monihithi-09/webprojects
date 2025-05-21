# OUALITY CONTROL IN MANUFACTURING

#base on size of the product ,checking the quality of the product


import random

# Define acceptable range for product size (e.g., in mm)
MIN_SIZE = 9.5
MAX_SIZE = 10.5

# Simulate measuring 20 manufactured items
def simulate_quality_control():
    passed = 0
    failed = 0
    results = []

    print("Quality Control Report:")
    print("-" * 30)
    for i in range(1, 21):
        # Simulate actual size between 9.0 and 11.0 mm
        size = round(random.uniform(9.0, 11.0), 2)

        # Check if the size is within acceptable range
        if MIN_SIZE <= size <= MAX_SIZE:
            status = "PASS"
            passed += 1
        else:
            status = "FAIL"
            failed += 1

        results.append((i, size, status))
        print(f"Item {i:02}: Size = {size} mm -> {status}")

    print("-" * 30)
    print(f"Total Passed: {passed}")
    print(f"Total Failed: {failed}")
    print("-" * 30)

    return results

# Run the simulation
simulate_quality_control()
