# Ejercicio 2

Inventario de una tienda 

Crear la clase Producto con nombre, precio y stock. Crear 4 productos e imprimirlos con el formato nombre : precio. Simular la venta de 3 unidades de dos de ellos, mostrar “Reponer” junto a cada producto que quede con menos de 5 unidades e imprimir el valor total del inventario (suma de precio por stock).

# Código 

class Producto {
    String nombre;
    double precio;
    int stock;

    public Producto(String nombre, double precio, int stock) {
        this.nombre = nombre;
        this.precio = precio;
        this.stock = stock;
    }
}

public class MainInventario {
    public static void main(String[] args) {
        Producto p1 = new Producto("Arroz", 1.50, 10);
        Producto p2 = new Producto("Aceite", 2.80, 4);
        Producto p3 = new Producto("Azúcar", 1.20, 6);
        Producto p4 = new Producto("Leche", 0.90, 3);

        System.out.println("--- Inventario Inicial ---");
        System.out.println(p1.nombre + ": $" + p1.precio);
        System.out.println(p2.nombre + ": $" + p2.precio);
        System.out.println(p3.nombre + ": $" + p3.precio);
        System.out.println(p4.nombre + ": $" + p4.precio);

        // Simular venta de 3 unidades de dos de ellos (ej. p1 y p2)
        p1.stock -= 3;
        p2.stock -= 3;

        System.out.println("\n--- Inventario Post-Venta ---");
        double valorTotal = 0;

        Producto[] lista = {p1, p2, p3, p4};
        for (Producto p : lista) {
            String alerta = (p.stock < 5) ? " Reponer" : "";
            System.out.println(p.nombre + ": Precio: $" + p.precio + ", Stock: " + p.stock + alerta);
            valorTotal += (p.precio * p.stock);
        }

        System.out.printf("\nValor total del inventario: $%.2f\n", valorTotal);
    }
}

# Evidencia}
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f34a9c69-b394-4890-95c7-40c8cbfa190b" />
