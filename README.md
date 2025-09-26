student_name = input()
current_gpa = input()
study_hours = input()
social_points = input()
stress_level = input()
print(f"Welcome to my game, {student_name}!")
print(f" ----- Your current stats are: ----- ")
print(f" Current GPA: {current_gpa:.2f}")
print(f" Student Hours: {study_hours}")
print(f" Social Points: {social_points}")
print(f" Stress Level: {stress_level}")
print(f"------------------------------------")

print("Choose your course load:")
print("A) Light (12 credits)")
print("B) Standard (15 credits)")
print("C) Heavy (18 credits)")
choice = input()
if choice == "A":
    if current_gpa >= 2.5:
        print("You can take a light load.")
        study_hours += 2
        stress_level += 10
    else:
        print("Your GPA is too low for a light load.")
elif choice == "B":
        if current_gpa >= 3.0:
            print("You can take a standard load.")
            study_hours += 4
            stress_level += 15
        else:
            print("Your GPA is too low for a standard load.")
elif choice == "C":
    if current_gpa >= 3.5:
        print("You can take a heavy load.")
        study_hours += 6
        stress_level += 25
    else:
        print("Your GPA is too low for a heavy load.")

else:
    print("Invalid choice. Defaulting to Standard load.")
    study_hours += 4
    stress_level += 15

print(f"\n ----- Stats after Decision 1 ----- ")
print(f" Current GPA: {current_gpa:.2f}")
print(f" Student Hours: {study_hours}")
print(f" Social Points: {social_points}")
print(f" Stress Level: {stress_level}")
print(f"------------------------------------")
study_options = ["Programming", "Math", "English", "History"]
subject_choice = input(f"Choose a subject to study {study_options}: ")
if subject_choice in study_options:
    print(f"You chose to study {subject_choice}.")
    if (subject_choice == "Programming" or subject_choice == "Math") and current_gpa >= 3.0:
        current_gpa += 1
        social_points += 8
        stress_level += 5
        print("Good job keeping your grades up! You have more time to hang with friends and less stress.")
    elif current_gpa < 3.0:
        current_gpa += 2
        social_points -=10
        stress_level += 10
        print("You worked extra hard to get your grades up, but at the cost of socializing and more stress.")
if (subject_choice == "English" or subject_choice == "History") and current_gpa >= 3.0:
    current_gpa += 1
    social_points += 10
    stress_level += 2
    print("Good job keeping your grades up! You have more time to hang with friends and less stress.")
elif current_gpa < 3.0:
    current_gpa += 2
    social_points -=5
    stress_level += 7
    print("You worked extra hard to get your grades up, but at the cost of socializing and more stress.")
