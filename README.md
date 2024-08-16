# Actividad-1-estructura-datos
import java.util.Scanner;

public class TiqueteAereo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Ingrese la edad de Ana (en años): ");
        int edadAna = scanner.nextInt();

        double precioTiquete = 1000000.0; // Precio base del tiquete

        if (edadAna < 2) {
            System.out.println("Ana es demasiado pequeña para viajar en avión.");
        } else if (edadAna >=2 && edadAna < 5) {
            System.out.println("Ana viaja gratis.");
        } else if (edadAna >=5 && edadAna < 11) {
            precioTiquete /= 2;
            System.out.println("El precio del tiquete para Ana es: $" + precioTiquete);
        } else if (edadAna >=11 && edadAna < 15) {
            precioTiquete *= 0.75; // 3/4 del precio normal
            System.out.println("El precio del tiquete para Ana es: $" + precioTiquete);
        } else {
            System.out.println("El precio del tiquete para Ana es: $" + precioTiquete);
        }

        scanner.close();
    }
}
