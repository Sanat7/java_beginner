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

       String[] myArray = new String[3];     // max. 3 Inhalte erlaubt

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

public class Main {
    public static void main(String[] args) {

       String[] myArray = {"AAA", "BBB", "CCC"};

       for (String inhalt : myArray) {          //durchlaufe in Array "myArray" und speichere die Inhalte in Typ "inhalt"
           System.out.println(inhalt);
       }
    }
}

*****************************************************************************************
// Mehrdimensionale Arrays : ***********************************************************

public class Main {
    public static void main(String[] args) {

       String[][] Lagerplatz = new String[3][2];   //3 va 2 lar 1 dan boshlab hisoblanadi 

        Lagerplatz[0][0] = "A1";
        Lagerplatz[0][1] = "A2";

        Lagerplatz[1][0] = "B1";
        Lagerplatz[1][1] = "B2";

        Lagerplatz[2][0] = "C1";
        Lagerplatz[2][1] = "C2";

       for (int i = 0; i < Lagerplatz.length; i++) {
           for (int j = 0; j < Lagerplatz[i].length; j++) {
            System.out.print(Lagerplatz[i][j] + " ");
           }
           System.out.println();
       }
    }
}

***************************************************************************************************
// Methoden: *************************************************************************************

public class Main {
    public static void main(String[] args) {

        System.out.println("Hiert kommt ein Method:");

        myMethod();
    }
    public static void myMethod() {        // void bedeutet kein Rückgabewert 
        int a = 5;
        int b = 10;
        System.out.println(a + b);
    }
}

****************************************************************************************************
// Methode mit Pareameter **************************************************************************

public class Main {
    public static void main(String[] args) {

        System.out.println("Hiert kommt ein Method:");

        myMethod(2, 5);
    }
    public static void myMethod(int parameter1, int parameter2) {
        int a = parameter1;
        int b = parameter2;
        System.out.println(a + b);
    }
}

********************************************************************************************************
// Methode mit Rückgabewert ****************************************************************************

public class Main {
    public static void main(String[] args) {

        System.out.println("Hiert kommt ein Method:");

        myMethod(2, 5);     //Ergebnis der Methode ist hier gespeichert, zeigt aber nicht
        System.out.println(myMethod(2, 5));    
    }
    public static int myMethod(int parameter1, int parameter2) {
        int a = parameter1 + parameter2;
        return a;
    }
}

***********************************************************************************************************
// Objekt Orientierte Programmierung(OOP)
// Klasse - Bauplan für Objekte 
// Attribute - Eigenschaften der Objekte 
// Methoden -  Funktionen der Objekte 

