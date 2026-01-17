# Encapsulation
// Student class demonstrating Encapsulation
public class Student {

    // Private data members (data hiding)
    private String name;
    private int age;
    private double cgpa;

    // Constructor
    public Student(String name, int age, double cgpa) {
        this.name = name;
        setAge(age);      // using setter for validation
        setCgpa(cgpa);    // using setter for validation
    }

    // Getter for name
    public String getName() {
        return name;
    }

    // Setter for name
    public void setName(String name) {
        this.name = name;
    }

    // Getter for age
    public int getAge() {
        return age;
    }

    // Setter for age with validation
    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        } else {
            System.out.println("Age must be positive!");
        }
    }

    // Getter for CGPA
    public double getCgpa() {
        return cgpa;
    }

    // Setter for CGPA with validation
    public void setCgpa(double cgpa) {
        if (cgpa >= 0.0 && cgpa <= 4.0) {
            this.cgpa = cgpa;
        } else {
            System.out.println("Invalid CGPA! Must be between 0.0 and 4.0");
        }
    }

    // Display student information
    public void displayInfo() {
        System.out.println("Name  : " + name);
        System.out.println("Age   : " + age);
        System.out.println("CGPA  : " + cgpa);
    }
}
// Main class to test Encapsulation
public class Main {
    public static void main(String[] args) {

        // Creating object using constructor
        Student student = new Student("Sadia Afrose", 21, 3.75);

        // Accessing data using public methods
        student.displayInfo();

        // Updating values using setters
        student.setAge(22);
        student.setCgpa(3.90);

        System.out.println("\nAfter Update:");
        student.displayInfo();

        // Trying invalid values
        student.setCgpa(5.0);   // Invalid CGPA
    }
}
