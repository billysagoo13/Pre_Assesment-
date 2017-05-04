# Pre_Assesment-
Ex1 &amp; Ex2 

import java.util.*;
public class main{
   public static void main(String args[]){
      ArrayList<familyMember> list = new ArrayList<familyMember>();
      Scanner scan = new Scanner(System.in);
      boolean isWed = false;
      System.out.println("Welcome to QA Cinemas please enter the day of the week: ");
      String ans = scan.nextLine();
      if(ans.toLowerCase().equals("wednesday")) //if the day they entered is wednesday set the boolean to true
         isWed = true;
      while(true){
         System.out.println("Enter 1 to buy a Standard Ticket"); //simple GUI to create familyMembers
         System.out.println("Enter 2 to buy an OAP Ticket"); 
         System.out.println("Enter 3 to buy a Student Ticket");
         System.out.println("Enter 4 to buy a Child Ticket");
         System.out.println("Enter -1 Exit");
         int an = scan.nextInt();
         if(an == -1)
            break;
         if(an == 1)
            list.add(new Standard());
         if(an == 2)
            list.add(new OAP());
         if(an == 3)
            list.add(new Student());
         if(an == 4)
            list.add(new Child());   
      }
      Family fam = new Family(list, isWed); //creating the family object and then printing it
      fam.print();
   }
}
