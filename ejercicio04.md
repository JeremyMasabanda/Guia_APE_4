# Ejercicio 4


Cuenta de ahorro

Crear la clase Cuenta con titular y saldo. Crear 2 cuentas, una con 200 y otra con 350. Con un while, depositar 50 por mes en cada cuenta hasta que llegue a 500,
imprimiendo cada mes con el formato titular : saldo, y al final cuántos meses necesitó cada una (6 y 3).

# Código

class Cuenta {
    String titular;
    double saldo;

    public Cuenta(String titular, double saldo) {
        this.titular = titular;
        this.saldo = saldo;
    }
}

public class MainCuentaAhorro {
    public static void main(String[] args) {
        Cuenta c1 = new Cuenta("Carlos", 200);
        Cuenta c2 = new Cuenta("Ana", 350);

        int mesesC1 = 0;
        int mesesC2 = 0;

        System.out.println("--- Simulación Cuenta 1 (" + c1.titular + ") ---");
        while (c1.saldo < 500) {
            c1.saldo += 50;
            mesesC1++;
            System.out.println(c1.titular + " : $" + c1.saldo);
        }

        System.out.println("\n--- Simulación Cuenta 2 (" + c2.titular + ") ---");
        while (c2.saldo < 500) {
            c2.saldo += 50;
            mesesC2++;
            System.out.println(c2.titular + " : $" + c2.saldo);
        }

        System.out.println("\n--- Resultados Finales ---");
        System.out.println(c1.titular + " necesitó " + mesesC1 + " meses.");
        System.out.println(c2.titular + " necesitó " + mesesC2 + " meses.");
    }
}

# Evidencia
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8d051a7d-009f-4548-b965-9854ad38872f" />
