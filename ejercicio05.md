# Ejercicio 5

Biblioteca

Crear las clases Libro (titulo, autor, disponible) y Socio (nombre, librosPrestados). Crear 4 libros y 2 socios, 
registrar que el primer socio presta 2 libros y el segundo presta 1 (disponible = false y aumentar librosPrestados), 
y al final imprimir cada libro con el formato titulo : Disponible o titulo : 
Prestado, cada socio con el formato nombre : librosPrestados y cuántos libros quedan disponibles.

# Código

class Libro {
    String titulo;
    String autor;
    boolean disponible;

    public Libro(String titulo, String autor) {
        this.titulo = titulo;
        this.autor = autor;
        this.disponible = true; // Por defecto inicia disponible
    }
}

class Socio {
    String nombre;
    int librosPrestados;

    public Socio(String nombre) {
        this.nombre = nombre;
        this.librosPrestados = 0;
    }
}

public class MainBiblioteca {
    public static void main(String[] args) {
        // Crear 4 libros
        Libro l1 = new Libro("Don Quijote", "Cervantes");
        Libro l2 = new Libro("Cien Años de Soledad", "García Márquez");
        Libro l3 = new Libro("El Principito", "Saint-Exupéry");
        Libro l4 = new Libro("La Odisea", "Homero");

        // Crear 2 socios
        Socio s1 = new Socio("Mateo");
        Socio s2 = new Socio("Lucía");

        // Primer socio presta 2 libros (ej: l1 y l2)
        l1.disponible = false;
        s1.librosPrestados++;
        l2.disponible = false;
        s1.librosPrestados++;

        // Segundo socio presta 1 libro (ej: l3)
        l3.disponible = false;
        s2.librosPrestados++;

        // Imprimir estado de los libros
        System.out.println("--- Estado de Libros ---");
        Libro[] libros = {l1, l2, l3, l4};
        int disponiblesCount = 0;
        
        for (Libro l : libros) {
            String estadoLibro = l.disponible ? "Disponible" : "Prestado";
            System.out.println(l.titulo + ": " + estadoLibro);
            if (l.disponible) {
                disponiblesCount++;
            }
        }

        // Imprimir estado de los socios
        System.out.println("\n--- Estado de Socios ---");
        Socio[] socios = {s1, s2};
        for (Socio s : socios) {
            System.out.println(s.nombre + ": " + s.librosPrestados + " libros prestados");
        }

        // Cantidad de libros disponibles al final
        System.out.println("\nCantidad de libros que quedan disponibles: " + disponiblesCount);
    }
}

# Evidencia 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6aef8212-cb9e-4425-812d-15a4590a20bb" />
