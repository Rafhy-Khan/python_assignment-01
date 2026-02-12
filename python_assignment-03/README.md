Python Control Flow: match-case, if-elif, and Nested if
Overview

This repository demonstrates modern Python decision-making constructs using:

match-case (introduced in Python 3.10)

Comparison between match-case and if-elif

Practical usage of nested if statements

The examples are structured, clean, and designed to strengthen conceptual clarity around conditional logic in Python.

1. Understanding match-case

match-case is a structural pattern matching feature introduced in Python 3.10.
It allows a variable to be matched against multiple patterns in a clean and readable way.

It is particularly useful when checking a single variable against fixed values.

Example 1: AI Mood Interpreter
# Program: Interpret AI emotional state based on input code

emotion_code = 2

match emotion_code:
    case 1:
        print("AI is in learning mode")
    case 2:
        print("AI is curious and exploring new ideas")
    case 3:
        print("AI is optimizing performance")
    case 4:
        print("AI is debugging reality")
    case _:
        print("Unknown AI state detected")

Example 2: Space Mission Control System
# Program: Decide spacecraft action based on signal received

signal = "LAND"

match signal:
    case "LAUNCH":
        print("Igniting boosters")
    case "ORBIT":
        print("Stabilizing orbit")
    case "LAND":
        print("Deploying landing gear")
    case "ABORT":
        print("Mission aborted safely")
    case _:
        print("Unknown command from mission control")

2. Difference Between match-case and if-elif
Key Differences
Feature	if-elif	match-case
Evaluates Conditions	Yes	No
Matches Fixed Values	Yes	Yes
Supports Range Checks	Yes	No
Pattern Matching	No	Yes
Introduced	Always in Python	Python 3.10
Example: Using if-elif for Range Checking
# Program: Analyze battery percentage using if-elif

battery = 75

if battery > 80:
    print("Battery Full")
elif battery > 50:
    print("Battery Moderate")
elif battery > 20:
    print("Battery Low")
else:
    print("Battery Critical")


This example works well because it evaluates conditions and ranges.

Example: Using match-case for Fixed Modes
# Program: Analyze exact battery modes using match-case

battery_mode = "ECO"

match battery_mode:
    case "PERFORMANCE":
        print("High performance mode activated")
    case "BALANCED":
        print("Balanced energy usage")
    case "ECO":
        print("Energy saving mode enabled")
    case _:
        print("Unknown battery mode")


This works best when matching exact values rather than evaluating expressions.

3. Nested if Statements

A nested if statement is an if inside another if.
It is useful when one condition must be checked only after another condition is satisfied.

Nested if statements are commonly used in:

Authentication systems

Permission validation

Game logic

Multi-level decision systems

Security checks

4. Five Mini Programs Using Nested if
1. Space Suit Readiness Check
# Program: Check astronaut readiness

oxygen_level = 85
helmet_on = True

if oxygen_level > 70:
    if helmet_on:
        print("Astronaut ready for spacewalk")
    else:
        print("Helmet missing. Cannot proceed")
else:
    print("Oxygen level too low")

2. Secure Login System
# Program: Two-level security check

password_correct = True
otp_verified = True

if password_correct:
    if otp_verified:
        print("Access granted")
    else:
        print("OTP verification failed")
else:
    print("Incorrect password")

3. Secret Game Level Unlock
# Program: Unlock secret level

score = 1200
has_key = True

if score > 1000:
    if has_key:
        print("Secret level unlocked")
    else:
        print("You need the golden key")
else:
    print("Score too low to unlock level")

4. Smart Climate Control
# Program: Smart temperature control

temperature = 30
humidity = 70

if temperature > 25:
    if humidity > 60:
        print("Turn on AC and dehumidifier")
    else:
        print("Turn on AC only")
else:
    print("Temperature is comfortable")

5. AI Response Moderation
# Program: AI response moderation

content_safe = True
contains_sensitive_topic = True

if content_safe:
    if contains_sensitive_topic:
        print("Respond carefully with context awareness")
    else:
        print("Respond normally")
else:
    print("Content blocked")

Conclusion

This repository demonstrates structured decision-making in Python using:

Modern pattern matching with match-case

Traditional conditional logic with if-elif

Layered decision systems with nested if

These constructs form the foundation of control flow in Python and are essential for building scalable and intelligent systems.
