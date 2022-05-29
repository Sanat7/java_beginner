# java_beginner 

**************************************************************************************************
1. While Schleife 

// Möglichkeit I:

public class Main {
    public static void main(String[] args) {
        int number = 1;

      while (number <= 10) {
          System.out.println("Die Nummern: " + number);
          number++;
      }
    }
 }


// Möglichkeit II:

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


// Möglichkeit III: 

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


// Möglichkeit IV:

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
2. For Schleife 

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
3. Random Klasse 

import java.util.Random;

public class Main {
    public static void main(String[] args) {
      Random myRandom = new Random();               // generiert die Zufallszahlen
      int zufallszahl = myRandom.nextInt();
      System.out.println(zufallszahl);
    }
}

*******************************************************************************************************************
4. Array:

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
5. Array Möglichkeit 2: 

public class Main {
    public static void main(String[] args) {

       String[] myArray = {"AAA", "BBB", "CCC"};

       for (int i = 0; i < myArray.length; i++) {
           System.out.println(myArray[i]);
       }
    }
}

*********************************************************************************
6. Foreach Schleife: 

public class Main {
    public static void main(String[] args) {

       String[] myArray = {"AAA", "BBB", "CCC"};

       for (String inhalt : myArray) {          //durchlaufe in Array "myArray" und speichere die Inhalte in Typ "inhalt"
           System.out.println(inhalt);
       }
    }
}

*****************************************************************************************
7. Mehrdimensionale Arrays : ***********************************************************

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
8. Methoden: *************************************************************************************

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
9. Methode mit Pareameter **************************************************************************

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
10. Methode mit Rückgabewert ****************************************************************************

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
11.  Objekt Orientierte Programmierung(OOP)
    // Klasse - Bauplan für Objekte 
    // Attribute - Eigenschaften der Objekte 
    // Methoden -  Funktionen der Objekte 
    
    
   //Hier ist Main Klasse: 
    
    public class Main {
    public static void main(String[] args) {

        Katze katzeObjekt = new Katze();

        katzeObjekt.miau();

        katzeObjekt.rechnen(10, 8);

    }

}

// Hier ist die Klasse Katze: 

public class Katze {

    //Attribute:
    int alter;
    String farbe;
    String rasse;
    boolean springen;

    //Methoden:
    public void miau() {
        System.out.println("Miauuuuu!!!");
    }

    public void rechnen(int zahl1, int zahl2) {
        System.out.println(zahl1 + zahl2);
    }

}

***************************************************************************************************************
12. Parameter übergeben:

// Main Klass (Hauptklasse): ------------------------------------------------------------------
public class Main {
    public static void main(String[] args) {
        
        //Attribute werden initialisiert: 
        Katze katzeObjekt = new Katze();
        katzeObjekt.alter = 3;
        katzeObjekt.farbe = "gelb";
        katzeObjekt.rasse = "heimisch";
        katzeObjekt.springen = true;

        katzeObjekt.test(true, "Miiiiiia!!!");


    }

}

// Klasse Katze: ----------------------------------------------------------------------------------------

public class Katze {

    //Attribute:
    int alter;
    String farbe;
    String rasse;
    boolean springen;

    //Methoden:
    public void miau(String machMiau) {     // miau Methode hat Parameter machMiau, hier übernimmt das Parameter machMiau den Parameter_2
        System.out.println(machMiau);
    }

    public void test(boolean Parameter_1, String Parameter_2) {      // test Methode hat 2 Parametern.
        if (Parameter_1) {                      //wenn Parameter_1 true ist, dann führe das Method miau.
            miau(Parameter_2);                  //miau übernimmt das Parameter_2.
        }
    }

}

********************************************************************************************************************************************
13. Konstruktor:

// Konstruktor dient die Attribute einfach zu initialisieren.


public class Main {
    public static void main(String[] args) {

        Katze katzeObjekt = new Katze(2, "gelb", "heimisch", true);
        System.out.println("katzeObjekt ist " + katzeObjekt.alter + " jahre alt");
    }
}

----------------------------------------------------------------------------------------------------------------------------
public class Katze {

    //Attribute:
    int alter;
    String farbe;
    String rasse;
    boolean springen;

    //Konstruktor:
    public Katze(int alter, String farbe, String rasse, boolean springen) {     //hier sind die Parametern mit gleichen Namen wie Attribute
        this.alter = alter;   //this bedeutet Attribute alter. Also Attribut this.alter übernimmt den Parameter alter.
        this.farbe = farbe;
        this.rasse = rasse;
        this.springen = springen;
    }
}

****************************************************************************************************************************
// Konstruktor.

public class Main {
    public static void main(String[] args) {

        Katze katzeObjekt = new Katze(2, "gelb", "heimisch", true);
        System.out.println("katzeObjekt ist " + katzeObjekt.alter + " jahre alt.");

        Katze mashka = new Katze(0.2, "schwarz", "unbekannt", true);
        System.out.print("Mashka ist " + mashka.alter + " Jahre alt, " + mashka.farbe + ", Rasse ist " + mashka.rasse + ", und kann ");
        if (mashka.springen) {
            System.out.print("springen.");
        } else {
            System.out.print("nicht springen, weil er noch jung ist.");
        }
    }
}

----------------------------------------------------------------------------------------------------------

public class Katze {

    //Attribute:
    double alter;
    String farbe;
    String rasse;
    boolean springen;
    
    //Konstruktor:
    public Katze(double alter, String farbe, String rasse, boolean springen) {     //hier sind die Parametern mit gleichen Namen wie Attribute
        this.alter = alter;   //this bedeutet Attribute alter. Also Attribut this.alter übernimmt den Parameter alter.
        this.farbe = farbe;
        this.rasse = rasse;
        this.springen = springen;
    }
}


***********************************************************************************************************************
14. Rückgabewert--------------------------------------------------------------------------------


public class Main {

    public static void main(String[] args) {        //void bedeutet, dass diese Methode kein Rückgabewert zurückgibt. 
        int summe = addition(5, 10);
        System.out.println(summe);
    }

    public static int addition(int zahl1, int zahl2) {     //ohne void gibt Methode einen Rückgabewert zurück.
        return zahl1 + zahl2;
    }
}



Rückgabewert -------------------------------------------------------------------------------------------------------------


public class Main {
    public static void main(String[] args) {
        Katze katze1 = fremdKatze(1);
    }

    public static Katze fremdKatze(int alter) {
        return new Katze(alter, "weiss", "qaymoq", true);
    }
}



-------------------------------------------------------------------------------------------------------------


public class Katze {
    //Attribute:
    double alter;
    String farbe;
    String rasse;
    boolean springen;

    //Konstruktor:
    public Katze(double alter, String farbe, String rasse, boolean springen) {     //hier sind die Parametern mit gleichen Namen wie Attribute
        this.alter = alter;   //this bedeutet Attribute alter. Also Attribut this.alter übernimmt den Parameter alter.
        this.farbe = farbe;
        this.rasse = rasse;
        this.springen = springen;
    }
}


**************************************************************************************************************
15. Überladung--------------------------------------------------------------------------------
     // mehrere Methoden mit gleicher Name, unterschiedlicher Parametern 



public class Main {
    public static void main(String[] args) {
        Kunde kunde1 = new Kunde("Xolid", "abc", 24, "Berlin");
        Kunde kunde2 = new Kunde("Sara", "sara1234"); 
    }
}


------------------------------------------------------------------------------------------------------------


public class Kunde {

    String name;
    String email;
    int age;
    String ort;

    public Kunde(String name, String email, int age, String ort) {
        this.name = name;
        this.email = email;
        this.age = age;
        this.ort = ort;
    }

    public Kunde(String name, String email) {
        this.name = name;
        this.email = email;
        this.age = 0;
        this.ort = "";
    }
}


*************************************************************************************************************

15. 


    


