import java.util.Scanner;

public class StudentGradeCalculatorJava {

   
    public static void  main (String[] args) {
        int numGrades;
        
        int[] grades;
        
        try (Scanner scanner = new Scanner(System.in))
        
        {
            System.out.print("Enter the number of grade: ");
            
            numGrades = scanner.nextInt();
            
            grades = new int[numGrades];
            
            for (int i = 0; i < numGrades; i++) {
                System.out.print("Enter the grades: " + (i + 1) + ": ");
                grades[i] = scanner.nextInt();
                
            }
        }

        int total = 0;
        for (int i = 0; i < numGrades; i++) {
            total += grades[i];
        }
        double average = (double) total / numGrades;

        System.out.println("Average Grade is : " + average);

    }
}
