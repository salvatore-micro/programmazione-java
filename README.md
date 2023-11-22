//inizio progamma principale
import java.util.Scanner;

public class TriangoloRettangolo {//inizio sottoprogamma
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Leggi tre valori numerici
        System.out.print("Inserisci il primo valore: ");
        double a = input.nextDouble();
        System.out.print("Inserisci il secondo valore: ");
        double b = input.nextDouble();
        System.out.print("Inserisci il terzo valore: ");
        double c = input.nextDouble();

        // Ordina i valori in ordine crescente
        if (a > b) {
            double temp = a;
            a = b;
            b = temp;
        }
        if (b > c) {
            double temp = b;
            b = c;
            c = temp;
        }

        // Verifica se a^2 + b^2 = c^2
        boolean isTriangoloRettangolo = (a * a + b * b == c * c);

        // Stampa il risultato
        if (isTriangoloRettangolo) {
            System.out.println("I tre valori possono essere le misure dei lati di un triangolo rettangolo.");
        } else {
            System.out.println("I tre valori non possono formare un triangolo rettangolo.");
        }

        input.close();
    }
}
//fine del programma 
