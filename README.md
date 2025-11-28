students = {}

while True:
    print("\n1. Add student")
    print("2. Add grade")
    print("3. Show grades")
    print("4. Exit")

    choice = input("Choose: ")

    if choice == "1":
        name = input("Student name: ")
        students[name] = []
        print("Student added.")

    elif choice == "2":
        name = input("Student name: ")
        if name in students:
            grade = float(input("Enter grade: "))
            students[name].append(grade)
            print("Grade added.")
        else:
            print("Student not found.")

    elif choice == "3":
        for name, grades in students.items():
            print(f"{name}: {grades}")

    elif choice == "4":
        print("Goodbye!")
        break

    else:
        print("Invalid choice.")
        
