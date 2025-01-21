# CaloriesCalculater

This code is a Java program that calculates an individual's Basal Metabolic Rate (BMR) and daily calorie needs based on their personal details and activity level. Here's a breakdown of its functionality:

# Note
    - Rename the package name
### Features and Functionality:
1. **Input Collection**:
   - Prompts the user to enter their gender (`M` or `F`), age, weight (in kilograms), height (in centimeters), and activity level (`sedentary`, `moderate`, or `active`).

2. **BMR Calculation**:
   - BMR is calculated using the **Harris-Benedict equation**:
     - For males:  
       \( BMR = 88.362 + (13.397 \times \text{weight}) + (4.799 \times \text{height}) - (5.677 \times \text{age}) \)
     - For females:  
       \( BMR = 447.593 + (9.247 \times \text{weight}) + (3.098 \times \text{height}) - (4.330 \times \text{age}) \)
   - The result is rounded to the nearest whole number.

3. **Daily Calorie Needs**:
   - The program adjusts the BMR based on the user's activity level:
     - **Sedentary**: \( \text{BMR} \times 1.2 \)
     - **Moderate**: \( \text{BMR} \times 1.55 \)
     - **Active**: \( \text{BMR} \times 1.725 \)
   - The activity level input is case-insensitive.

4. **Validation**:
   - If the user enters invalid data for gender or activity level, the program displays an error message and terminates.

5. **Output**:
   - Displays:
     - The calculated **BMR** in calories per day.
     - The estimated **daily calorie needs** based on the activity level.

6. **Closing Resources**:
   - Ensures the `Scanner` object is properly closed after input collection.

### Example Usage:
```
Calorie Calculator
Enter your gender (M/F): M
Enter your age: 25
Enter your weight in kilograms: 70
Enter your height in centimeters: 175
Enter your activity level (sedentary/moderate/active): moderate
```

**Output**:
```
Your Basal Metabolic Rate (BMR) is: 1661 calories per day.
Your estimated daily calorie needs are: 2575 calories per day.
```

### Key Notes:
- The program uses the `Scanner` class for input and ensures type-appropriate data is collected.
- It handles invalid inputs for gender and activity level gracefully by showing an error message.
- The formula used is suitable for estimating energy expenditure but may not account for all individual differences.