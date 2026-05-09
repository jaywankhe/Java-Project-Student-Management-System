# Java-Project-Student-Management-System
Features
* Add Student
* View Students
* Search Student
* Delete Student
  
  Technologies
* Java
* ArrayList
* OOP Concepts<img width="1523" height="1026" alt="Screenshot 2026-05-09 115653" src="https://github.com/user-attachments/assets/46760fd3-7e5b-4d5c-b015-d686e581d164" />

CODE :-
import java.util.*;

class Student {
    int id;
    String name;

    Student(int id, String name) {
        this.id = id;
        this.name = name;
    }
}

public class StudentManagement {
    public static void main(String[] args) {

        ArrayList<Student> students = new ArrayList<Student>();
        Scanner sc = new Scanner(System.in);

        while (true) {

            System.out.println("1. Add Student");
            System.out.println("2. View Students");
            System.out.println("3. Exit");

            System.out.print("Enter Choice: ");
            int choice = sc.nextInt();

            switch(choice) {

                case 1:
                    System.out.print("Enter ID: ");
                    int id = sc.nextInt();

                    sc.nextLine();

                    System.out.print("Enter Name: ");
                    String name = sc.nextLine();

                    students.add(new Student(id, name));

                    System.out.println("Student Added Successfully!");
                    break;

                case 2:
                    System.out.println("Student List:");

                    for(Student s : students) {
                        System.out.println(s.id + " - " + s.name);
                    }
                    break;

                case 3:
                    System.out.println("Exiting Program...");
                    System.exit(0);
                    break;

                default:
                    System.out.println("Invalid Choice!");
            }
        }
    }
}
