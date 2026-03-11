class Student:
    def __init__(self, roll, name, marks):
        self.roll = roll
        self.name = name
        self.marks = marks

    def display(self):
        print("Roll No:", self.roll)
        print("Name:", self.name)
        print("Marks:", self.marks)
        print("----------------------")


class StudentManager:
    def __init__(self):
        self.students = []

    def add_student(self):
        roll = int(input("Enter Roll Number: "))
        name = input("Enter Name: ")
        marks = float(input("Enter Marks: "))

        student = Student(roll, name, marks)
        self.students.append(student)
        print("Student Added Successfully\n")

    def show_students(self):
        if len(self.students) == 0:
            print("No student records found\n")
        else:
            for s in self.students:
                s.display()

    def search_student(self):
        r = int(input("Enter Roll Number to Search: "))
        found = False

        for s in self.students:
            if s.roll == r:
                s.display()
                found = True
                break

        if not found:
            print("Student Not Found\n")

    def delete_student(self):
        r = int(input("Enter Roll Number to Delete: "))
        for s in self.students:
            if s.roll == r:
                self.students.remove(s)
                print("Student Deleted\n")
                return

        print("Student Not Found\n")

    def update_marks(self):
        r = int(input("Enter Roll Number to Update Marks: "))
        for s in self.students:
            if s.roll == r:
                new_marks = float(input("Enter New Marks: "))
                s.marks = new_marks
                print("Marks Updated\n")
                return

        print("Student Not Found\n")


def main():
    manager = StudentManager()

    while True:
        print("===== Student Management System =====")
        print("1. Add Student")
        print("2. Show All Students")
        print("3. Search Student")
        print("4. Delete Student")
        print("5. Update Marks")
        print("6. Exit")

        choice = input("Enter Your Choice: ")

        if choice == "1":
            manager.add_student()
        elif choice == "2":
            manager.show_students()
        elif choice == "3":
            manager.search_student()
        elif choice == "4":
            manager.delete_student()
        elif choice == "5":
            manager.update_marks()
        elif choice == "6":
            print("Exiting Program...")
            break
        else:
            print("Invalid Choice\n")


if __name__ == "__main__":
    main()
