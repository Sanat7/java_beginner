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
      System.out.println("Beendet");
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


// While Schleife:

public class Main {
    public static void main(String[] args) {
    
        int zahl = 1;

        while(zahl <=10){
            System.out.println(zahl);
            zahl++; 
        }
    }
}



// Do-While Schlaife:

public class Main {
    public static void main(String[] args) {
        int zahl = 1;

        do {                            // erst einmal durchführung dann die Bedingung achten
            System.out.println(zahl);
            zahl++;
        }
        while(zahl <= 10); 
    }
}


// Verschachtelte Schleifen:

public class Main {
    public static void main(String[] args) {

        for (int i = 0; i < 4; i++) {
            for (int j = 0; j < 6; j++) {
                System.out.print(j);
            }
            System.out.println();
        }
    }
}

************************************************************************************************************
// Random Klasse 

import java.util.Random;

public class Main {
    public static void main(String[] args) {
      Random myRandom = new Random();               // generiert die Zufallszahlen
      int zufallszahl = myRandom.nextInt();
      System.out.println(zufallszahl);
    }
}

*******************************************************************************************************************
// Array:

import java.sql.Array;

public class Main {
    public static void main(String[] args) {

       String[] myArray = new String[3];

       myArray[0] = "AAA";
       myArray[1] = "BBB";
       myArray[2] = "CCC";

       for (int i = 0; i < myArray.length; i++) {
           System.out.println(myArray[i]);
       }
    }
}

******************************************************************************************
// Array Möglichkeit 2: 

public class Main {
    public static void main(String[] args) {

       String[] myArray = {"AAA", "BBB", "CCC"};

       for (int i = 0; i < myArray.length; i++) {
           System.out.println(myArray[i]);
       }
    }
}

*********************************************************************************
// Foreach Schleife: 


