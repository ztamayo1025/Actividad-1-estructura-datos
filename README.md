# Actividad-1-estructura-datos
import java.util.Scanner;

public class CalculadoraPrecioTiquete {

    public static void main(String[] args) {
        double precioBase = 1000000.00;
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese la edad de Ana: ");
        String edadString = scanner.nextLine();
        int edad = Integer.parseInt(edadString);
        double precioTiquete = 0.0;

        if (edad < 2) {
            System.out.println("Prohibido viajar");
        } else if (edad >= 2 && edad < 5) {
            System.out.println("El tiquete es gratuito");
        } else if (edad >= 5 && edad < 11) {
            precioTiquete = precioBase / 2; // 1/2 precio
            System.out.println("El valor del tiquete es: $" + precioTiquete);
        } else {
            precioTiquete = (precioBase * 3) / 4; // 3/4 precio
            System.out.println("El valor del tiquete es: $" + precioTiquete);
        }

        scanner.close();
    }
}
