# java_beginner 

**************************************************************************************************
// While Schleife 

// 1. Möglichkeit:

public class Main {
    public static void main(String[] args) {
        int number = 1;

      while (number <= 10) {
          System.out.println("Die Nummern: " + number);
          number++;
      }
    }
 }


// 2. Möglichkeit:

public class Main {
    public static void main(String[] args) {
        int number = 1;
        boolean cont = true;

      while (cont) {
          System.out.println("Die Nummern: " + number);
          number++;
          if (number == 10) {
              cont = false;    // alternativ kann man "break;" verwenden
          }
      }
    }
}


// 3. Möglichkeit: 

public class Main {
    public static void main(String[] args) {
        int number = 1;

      while (true) {
          System.out.println("Die Nummern: " + number);
          number++;
          if (number > 10) {
              break;
          }
      }
    }
}


// 4. Möglichkeit:

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner wahl = new Scanner(System.in);
        int wieder = 1;

      while (wieder == 1) {
          System.out.println("hier ist das zu wiederholende Objekt ");
          System.out.println("Möchtest du wiederholen? für ja bitte 1 drüken.");
          wieder = wahl.nextInt();
      }
      System.out.println("Beendet.");
    }
}

***********************************************************************************************************
// For Schleife 

public class Main {
    public static void main(String[] args) {
        for (int i = 0; i < 10; i+=2) {
            System.out.println("Zahl - " + i);
        }
    }
}

************************************************************************************************************
// Random Klasse 


