# Ejercicio 1

**Notas del curso**

Crear la clase Estudiante con los atributos nombre, nota1, nota2, nota3 y promedio. En main, crear 5 instancias, 
calcular el promedio de cada una e imprimirlas una debajo de otra con el formato nombre : promedio, agregando Aprobado (7 o más), 
Supletorio (de 5 a 6.99) o Reprobado (menos de 5). Al final, imprimir cuántos estudiantes aprobaron.

# Codigo 


import java.util.Scanner;

class Estudiante {
    String nombre;
    double nota1;
    double nota2;
    double nota3;
    double promedio;

    public Estudiante(String nombre, double nota1,
                      double nota2, double nota3) {
        this.nombre = nombre;
        this.nota1 = nota1;
        this.nota2 = nota2;
        this.nota3 = nota3;
    }

    public void calcularPromedio() {
        promedio = (nota1 + nota2 + nota3) / 3;
    }
}

public class Ejercicio1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Estudiante[] estudiantes = new Estudiante[5];
        int aprobados = 0;

        for (int i = 0; i < estudiantes.length; i++) {
            System.out.println("\nEstudiante " + (i + 1));

            System.out.print("Ingrese el nombre: ");
            String nombre = sc.nextLine();

            System.out.print("Ingrese la primera nota: ");
            double nota1 = sc.nextDouble();

            System.out.print("Ingrese la segunda nota: ");
            double nota2 = sc.nextDouble();

            System.out.print("Ingrese la tercera nota: ");
            double nota3 = sc.nextDouble();
            sc.nextLine();

            estudiantes[i] = new Estudiante(
                    nombre, nota1, nota2, nota3);
        }

        System.out.println("\n--- RESULTADOS ---");

        for (Estudiante e : estudiantes) {
            e.calcularPromedio();

            System.out.printf("%s : %.2f",
                    e.nombre, e.promedio);

            if (e.promedio >= 7) {
                System.out.println(" - Aprobado");
                aprobados++;
            } else if (e.promedio >= 5) {
                System.out.println(" - Supletorio");
            } else {
                System.out.println(" - Reprobado");
            }
        }

        System.out.println("Total de aprobados: " + aprobados);

        sc.close();
    }
}

# Evidencia
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/661b1f59-1339-450c-9b4d-82f243da98bf" />
