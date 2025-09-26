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
if subject_choice not in study_options:
    print("Pick a study choice that is listed.")
    print(f" ----- Stats after Decision 2: ----- ")
    print(f" Current GPA: {current_gpa:.2f}")
    print(f" Student Hours: {study_hours}")
    print(f" Social Points: {social_points}")
    print(f" Stress Level: {stress_level}")
    print(f"------------------------------------")
    if choice == "A":
        if study_hours >= 20 and stress_level >= 40:
            study_hours += 5
            stress_level += 10
            social_points -= 10
            print("You did not expect such a workload, and the stress is getting to you.")
        elif study_hours < 15 or stress_level < 20:
            study_hours -= 5
            stress_level -= 10
            social_points += 10
            print("You are glad you took this path, you have more time to socialize and make time for yourself.")
    if choice == "B":
        if study_hours >= 20 and stress_level >= 40:
                study_hours += 3
                stress_level += 5
                social_points -= 5
                print("You somewhat expecting this workload, but it still drags you down a bit.")
        elif study_hours < 15 or stress_level < 20:
            study_hours -= 2
            stress_level -= 8
            social_points += 15
            print("Your workload was a little less rigirous than you expected, and you have some more time than usual for yourself.")
    if choice == "C":
        if study_hours >= 20 and stress_level >= 40:
            study_hours += 2
            stress_level += 3
            social_points -= 4
            print("You completely expected this heavy workload, so you arentaffecting at all by your busy schedule.")
    elif study_hours < 15 or stress_level < 20:
        stress_level -= 25
        social_points += 30
        print("You worked extremely hard to overcome your busy workload,and you deserve time for yourself, family and friends more than anyone else.")
print(f" ----- Stats after Decision 2: ----- ")
print(f" Current GPA: {current_gpa:.2f}")
print(f" Student Hours: {study_hours}")
print(f" Social Points: {social_points}")
print(f" Stress Level: {stress_level}")
print(f"------------------------------------")
opportunity_type = ["Research", "Sports"]
research_opportunity = "Research"
sports_oppurtunity = "Sports"
if opportunity_type is research_opportunity:
    print("You got a research opportunity! This could boost your GPA.")
    current_gpa += 0.5
else:
    print("No research opportunities came your way this semester.")
if opportunity_type is not research_opportunity:
    print("You missed the research opportunity and focused elsewhere.")
    social_points += 5
if opportunity_type is sports_oppurtunity:
    print("You got a sports opportunity! This could boost your social life.")
    social_points += 15
else:
    print("No sports opportunities came your way this semester.")
if opportunity_type is not research_opportunity:
    print("You missed the sports opportunity and focused elsewhere.")
current_gpa += 0.25
print(f"\n ----- Stats after Decision 3 ----- ")
print(f" Current GPA: {current_gpa:.2f}")
print(f" Student Hours: {study_hours}")
print(f" Social Points: {social_points}")
print(f" Stress Level: {stress_level}")
print(f"------------------------------------")
