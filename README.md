student_name = "Ramiyah Davidson"
current_gpa = 3.9 #float between 1.0-4.0
study_hours = 60 #integer
social_points = 60 #integer
stress_level = 78 #integer between 1-100

#Displayed welcome STATS

print(f"WELCOME {student_name} TO YOUR ACADEMIC PROFILE!")
print("Your current stats")
print(f"Current Gpa: {current_gpa}")
print(f"Study Hours: {study_hours}")
print(f"Social Points: {social_points}")
print(f"Stress Level: {stress_level}")

 print(f"\n Choose your course load:")
print(f"A) Light Work (12 credits)")
print(f"B) Normal (15 credits)")
print(f"C) Pushing it  (18 credits)")
choice = input("Your choice:")

if choice == "A":
    if current_gpa >= 3.5:
        study_hours = study_hours - 3
        stress_level = stress_level - 5
    else:
        study_hours = study_hours - 1
        stress_level = stress_level - 2
elif choice == "B":
    if current_gpa >= 3.0:
        study_hours = study_hours + 2
        stress_level = stress_level + 5
    else:
        study_hours = study_hours + 4
        stress_level = stress_level + 9 
elif choice == "C":
    if current_gpa >= 3.5:
        study_hours = study_hours + 5
        stress_level = stress_level + 11
    else: 
        study_hours = study_hours + 10
        stress_level = stress_level + 20
else:
    ("Invalid Course Load")
