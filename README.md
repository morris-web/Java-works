import java.util.Scanner;
public class Main {
public static void main(String[] args) {
Scanner input = new Scanner(System.in);
int numberOfStudents;
System.out.println("Enter the number of students: ");
numberOfStudents = input.nextInt();
int[] indexNumbers = new int[numberOfStudents];
double[] midSemesterMarks = new double[numberOfStudents];
double[] endOfSemesterMarks = new

double[numberOfStudents];

double[] finalMarks = new double[numberOfStudents];
String[] grades = new String[numberOfStudents];
for (int i = 0; i < numberOfStudents; i++) {
System.out.println("Enter index number of student " + (i

+ 1));

indexNumbers[i] = input.nextInt();
System.out.println("Enter mid-semester mark of student "

+ (i + 1));

midSemesterMarks[i] = input.nextDouble();
System.out.println("Enter end-of-semester mark of student

" + (i + 1));

endOfSemesterMarks[i] = input.nextDouble();
finalMarks[i] = (midSemesterMarks[i] / 100 * 30) +
(endOfSemesterMarks[i] / 100 * 70);
if (finalMarks[i] >= 70) {
grades[i] = "A";
} else if (finalMarks[i] >= 60) {
grades[i] = "B";
} else if (finalMarks[i] >= 50) {
grades[i] = "C";
} else if (finalMarks[i] >= 40) {
grades[i] = "D";
} else {

grades[i] = "F";
}
}
System.out.println("Final scores of each student: ");
for (int i = 0; i < numberOfStudents; i++) {
System.out.println("Index number: " + indexNumbers[i] + "
Final score: " + finalMarks[i]);
}
System.out.println("Grades obtained by each student: ");
for (int i = 0; i < numberOfStudents; i++) {
System.out.println("Index number: " + indexNumbers[i] + "
Grade: " + grades[i]);
}
System.out.println("Table showing a candidate's index no., final
score, and grade obtained:");
System.out.println("+" + "------------" + "+" + "-------------" +
"+" + "-------" + "+");
System.out.println("|" + " Index No. " + "|" + " Final Score " +
"|" + " Grade " + "|");
System.out.println("+" + "------------" + "+" + "-------------" +
"+" + "-------" + "+");
for (int i = 0; i < numberOfStudents; i++) {
System.out.println("| "+indexNumbers[i] + " |" + finalMarks[i] + "
|" + grades[i]+" |");
}
System.out.println("+" + "------------" + "+" + "-------------" +
"+" + "-------" + "+");
}
}
