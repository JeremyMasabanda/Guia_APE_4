# Ejercicio 3

Veterinaria

Crear la clase Mascota con nombre, especie, edad y peso. 
Crear 3 mascotas e imprimirlas con el formato nombre : especie : peso, mostrando “Revisar peso” si pesan más de 20 kg. 
Luego escribir Mascota m4 = m1;, sumar 1 a m4.edad, imprimir m1.edad y explicar en un comentario por qué cambió.

# Código 

class Mascota {
    String nombre;
    String especie;
    int edad;
    double peso;

    public Mascota(String nombre, String especie, int edad, double peso) {
        this.nombre = nombre;
        this.especie = especie;
        this.edad = edad;
        this.peso = peso;
    }
}

public class MainVeterinaria {
    public static void main(String[] args) {
        Mascota m1 = new Mascota("Firulais", "Perro", 3, 22.5);
        Mascota m2 = new Mascota("Michi", "Gato", 2, 4.0);
        Mascota m3 = new Mascota("Rocky", "Perro", 5, 25.0);

        Mascota[] mascotas = {m1, m2, m3};

        System.out.println("--- Lista de Mascotas ---");
        for (Mascota m : mascotas) {
            String alertaPeso = (m.peso > 20) ? " Revisar peso" : "";
            System.out.println(m.nombre + ": " + m.especie + ": " + m.peso + " kg" + alertaPeso);
        }

        // Asignación de referencia
        Mascota m4 = m1;
        m4.edad += 1; // Sumar 1 a la edad a través de m4

        System.out.println("\nEdad de m1 después de modificar m4: " + m1.edad);
        
        /* 
         * Explicación: 
         * Por qué cambió m1.edad? 
         * En Java, los objetos se manipulan mediante referencias (apuntadores en memoria). 
         * Al escribir "Mascota m4 = m1;", no se está copiando el objeto en sí, sino que 
         * m4 pasa a apuntar exactamente a la misma posición de memoria que m1. 
         * Por lo tanto, cualquier cambio realizado en la edad a través de m4 se refleja 
         * directamente en m1 porque ambos hacen referencia al mismo objeto.
         */
    }
}

# Evidencia
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b65586dd-01aa-4534-845a-5bb0d9f71242" />
