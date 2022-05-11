# HawaiianWords
import java.util.Scanner; 

public class Main {
  public static void main(String[] args) {
    boolean bool = true;
    while (bool == true) {
      System.out.print("Enter a hawaiian word to pronounce: ");
      Scanner keyboard  = new Scanner(System.in).useDelimiter("\n"); 
      String hawaiian = keyboard.next(); 
      String hawaii = makeWord(hawaiian); 
      System.out.println(hawaii);
      boolean correct = false; 
      while (correct == false) {
        System.out.print("Would you like to enter another word?: ");
        String answer = keyboard.next(); 
        answer = answer.toLowerCase();  
        if(answer.equals("yes") || answer.equals("y")) {
          bool = true;
          correct = true; 
        } else if (answer.equals("no") || answer.equals("n")) {
            bool = false; 
            correct = true; 
          }
        else {
          System.out.print("valid answers are yes,y,no, or n in either capital or lowercase. please tell your answer: ");
          answer = keyboard.next();
          answer = answer.toLowerCase(); 
          if(answer.equals("yes") || answer.equals("y")) {
            correct = true; 
          }
          else if (answer.equals("no") || answer.equals("n")) {
            correct = false; 
            bool = false; 
          }
        }
      }
    }
  }
  public static String makeWord(String hawaiian) {
    hawaiian = hawaiian.toLowerCase(); 
    boolean check = true;
    char[] bank = {'a','e','i','o','u','p','k','h','l','m','n','w',' ','\''};
    int count = 0;
    for(int i = 0; i < hawaiian.length(); i++) {
      char each = hawaiian.charAt(i); 
      for(int j = 0; j < bank.length; j++) {
        if (each != bank[j]){
          count++;
        }
        if (count == 14) {
          check = false;
        }
      }
      count = 0;
    }
    String hawaii = "";
    String hawaii2 = ""; 
    if (check == false) {
      hawaii = "invalid";
    }
    else if (check == true) {
      hawaii = hawaiian.toUpperCase() + " is pronounced ";
      String w = "w";
      String wAfter = "v";
      String a = "ah";
      String e = "eh"; 
      String i = "ee";
      String o = "oh";
      String u = "oo";
      String ai = "eye";
      String ae = "eye";
      String ao = "ow";
      String au = "ow";
      String ei = "ay";
      String eu = "eh-oo";
      String iu = "ew";
      String oi = "oy";
      String ou = "ow";
      String ui = "ooey";
      String space = " ";
      String apostrophe = "'";
      char temp = ' ';
      hawaiian = hawaiian.toLowerCase();
      for (int z = 0; z < hawaiian.length(); z++) {
        if (hawaiian.charAt(z) == 'a' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) == 'i') {
          hawaii2 += ai;
          z++;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'a' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) == 'e') {
          hawaii2 += ae;
          z++;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'a' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) == 'o') {
          hawaii2 += ao;
          z++;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'a' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) == 'u') {
          hawaii2 += au;
          z = z++;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'a' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) != 'i' && hawaiian.charAt(z + 1) != 'i' && hawaiian.charAt(z + 1) != 'o' && hawaiian.charAt(z + 1) != 'u') {
          hawaii2 += a;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'a' && z == hawaiian.length() - 1) {
          hawaii2 += a;
        }
        // next line
        if (hawaiian.charAt(z) == 'e' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) == 'i') {
          hawaii2 += ei;
          z++;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'e' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) == 'u') {
          hawaii2 += eu;
          z++;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'e' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) != 'i' && hawaiian.charAt(z + 1) != 'u') {
          hawaii2 += e;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'e' && z == hawaiian.length() - 1 && hawaiian.charAt(z - 1) != 'a') {
          hawaii2 += e;
        }
        // new line
        if (hawaiian.charAt(z) == 'o' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) == 'i') {
          hawaii2 += oi;
          z++;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'o' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) == 'u') {
          hawaii2 += ou;
          z++;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'o' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) != 'i' && hawaiian.charAt(z + 1) != 'u') {
          hawaii2 += o;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'o' && z == hawaiian.length() - 1 && hawaiian.charAt(z - 1) != 'a') {
          hawaii2 += o;
        }
        // new line
        if (hawaiian.charAt(z) == 'u' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) == 'i') {
          hawaii2 += ui;
          z++;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'u' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) != 'i') {
          hawaii2 += u;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'u' && z == hawaiian.length() - 1 && hawaiian.charAt(z - 1) != 'a' && hawaiian.charAt(z - 1) != 'i' && hawaiian.charAt(z - 1) != 'o') {
          hawaii2 += u;
        }
        // new line
        if (hawaiian.charAt(z) == 'i' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) == 'u') {
          hawaii2 += iu;
          z++;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'i' && z != hawaiian.length() - 1 && hawaiian.charAt(z + 1) != 'u') {
          hawaii2 += i;
          if (z != hawaiian.length() - 1 && (hawaiian.charAt(z + 1) != '\'' && hawaiian.charAt(z + 1) != ' ')) {
            hawaii2 += "-";
          }
        }
        if (hawaiian.charAt(z) == 'i' && z == hawaiian.length() - 1 && hawaiian.charAt(z - 1) != 'a' && hawaiian.charAt(z - 1) != 'e' && hawaiian.charAt(z - 1) != 'o' && hawaiian.charAt(z - 1) != 'u') {
          hawaii2 += i;
        }
        // new line
        if (hawaiian.charAt(z) == 'p' || hawaiian.charAt(z) == 'k' || hawaiian.charAt(z) == 'h' || hawaiian.charAt(z) == 'l' || hawaiian.charAt(z) == 'm' || hawaiian.charAt(z) == 'n') {
          temp = hawaiian.charAt(z); 
          hawaii2 += temp; 
        }
        // new line
        if (hawaiian.charAt(z) == 'w') {
          if(z >= 1 && (hawaiian.charAt(z-1) == 'e' || hawaiian.charAt(z-1) == 'i')) {
            hawaii2 += wAfter;
          } else {
            hawaii2 += w;  
          }
        }
        // new line
        if (hawaiian.charAt(z) == ' ') {
          hawaii2 += " ";
        }
        if (hawaiian.charAt(z) == '\'') {
          hawaii2 += "'";
        }
      }
      // write the hawaii2 --> hawaii here
      hawaii2 = hawaii2.substring(0,1).toUpperCase() + hawaii2.substring(1);
      hawaii += hawaii2;
    }
    return hawaii; 
  }
}
