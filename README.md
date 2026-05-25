# PIZZA-HUT.
import java.util.Scanner;
public class PizzaHut {
    public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    System.out.println("=======================");
    System.out.println("       Pizza Hut       ");
    System.out.println("=======================");
    System.out.println("Ingrese su nombre:");
    String nombre = sc.nextLine();
    bienvenida(nombre);
    System.out.println("Seleccione en (numero)");
    System.out.println("1.-Entrar como Invitado");
    System.out.println("2.-Registrarse");
    System.out.println("3.-Salir");
    int opcion = sc.nextInt();
    switch(opcion){
            case 1:
                invitado();
                menuPrincipal(sc);
                break;
            case 2:
                registrarse(sc);
                menuPrincipal(sc);
                break;
            case 3:
                System.out.println("Gracias por visitar Pizza Hut");
                break;
            default:
                System.out.println("Opcion invalida");
        }
    }
    public static void bienvenida(String nombre){
        System.out.println("Bienvenido a Pizza Hut: " + nombre);
    }
    public static void invitado(){
        System.out.println("Ingresaste como invitado");
    }
    public static void registrarse(Scanner sc){
        sc.nextLine();
        System.out.println("=====REGISTRO=====");
        System.out.println("Ingrese su Nombre :");
        String nombre = sc.nextLine();
        System.out.println("Ingrese Apellido:");
        String apellido = sc.nextLine();
        System.out.println("Ingrese su N°de Celular:");
        int celular = sc.nextInt();
        System.out.println("Ingrese su DNI:");
        int dni = sc.nextInt();

        System.out.println("===DATOS REGISTRADOS===");
        System.out.println("Nombre:"+nombre);
        System.out.println("Apellido:"+apellido);
        System.out.println("Celular:"+celular);
        System.out.println("DNI:"+dni);
    }
    public static double menuPrincipal(Scanner sc) {
        System.out.println("=====Menu del Momento=====");
        System.out.println("1.-Carta:");
        System.out.println("2.-Promociones:");
        System.out.println("3.-Ir a iniciar sesion:");
        int opcion = sc.nextInt();
        switch (opcion) {
            case 1:
                double precio = 0;
                System.out.println("=====Carta=====");
                System.out.println("1.-Pizza");
                System.out.println("2.-Antojitos");
                System.out.println("3.-Bebidas");
                int ofrece = sc.nextInt();
                switch (ofrece) {
                    case 1:
                        int opcionPizza;
                        int opcionTamaño;
                        System.out.println("=====Pizza=====");
                        System.out.println("1. Pizza Americana");
                        System.out.println("2. Pizza Chicken BBQ");
                        System.out.println("3. Pizza Chili Hut");
                        System.out.println("4. Pizza Continental");
                        System.out.println("5. Pizza Hawaiana");
                        System.out.println("6. Pizza Meat Lovers");
                        System.out.println("7. Pizza Mozzarella");
                        System.out.println("8. Pizza Pepperoni");
                        System.out.println("9. Pizza Vegetariana");
                        System.out.println("10. Pizza Suprema");
                        System.out.print("Seleccione una pizza: ");
                        opcionPizza = sc.nextInt();
                        System.out.println("Seleccione el tamaño:");
                        System.out.println("1. Mediana");
                        System.out.println("2. Grande");
                        System.out.println("3. Familiar");
                        System.out.print("Opción: ");
                        opcionTamaño = sc.nextInt();
                        switch (opcionPizza) {
                            case 1: //pizza Americana
                                switch (opcionTamaño) {
                                    case 1: precio = 22.90; break;
                                    case 2: precio = 29.90; break;
                                    case 3: precio = 39.90; break;
                                }
                                break;
                            case 2: //pizza Chicken BBQ
                                switch (opcionTamaño) {
                                    case 1: precio = 32.90; break;
                                    case 2: precio = 41.90; break;
                                    case 3: precio = 51.90; break;
                                }
                                break;
                            case 3: //pizza Chili Hut
                                switch (opcionTamaño) {
                                    case 1: precio = 32.90; break;
                                    case 2: precio = 41.90; break;
                                    case 3: precio = 51.90; break;
                                }
                                break;
                            case 4: //pizza Continental
                                switch (opcionTamaño) {
                                    case 1: precio = 27.90; break;
                                    case 2: precio = 34.90; break;
                                    case 3: precio = 44.90; break;
                                }
                                break;
                            case 5: //pizza Hawaiana
                                switch (opcionTamaño) {
                                    case 1: precio = 27.90; break;
                                    case 2: precio = 34.90; break;
                                    case 3: precio = 44.90; break;
                                }
                                break;
                            case 6: //pizza Meat Lovers
                                switch (opcionTamaño) {
                                    case 1: precio = 32.90; break;
                                    case 2: precio = 41.90; break;
                                    case 3: precio = 51.90; break;
                                }
                                break;
                            case 7: //pizza Mozzarella
                                switch (opcionTamaño) {
                                    case 1: precio = 22.90; break;
                                    case 2: precio = 29.90; break;
                                    case 3: precio = 39.90; break;
                                }
                                break;
                            case 8: //pizza Pepperoni
                                switch (opcionTamaño) {
                                    case 1: precio = 22.90; break;
                                    case 2: precio = 29.90; break;
                                    case 3: precio = 39.90; break;
                                }
                                break;
                            case 9: //pizza vegetariana
                                switch (opcionTamaño) {
                                    case 1: precio = 27.90; break;
                                    case 2: precio = 34.90; break;
                                    case 3: precio = 44.90; break;
                                }
                                break;
                            case 10: //pizza suprema
                                switch (opcionTamaño) {
                                    case 1: precio = 27.90; break;
                                    case 2: precio = 34.90; break;
                                    case 3: precio = 44.90; break;
                                }
                                break;
                            default:
                                System.out.println("Opción inválida.");
                        }
                        return precio;
                    case 2:
                        System.out.println("=====Antojitos=====");
                        break;
                    case 3:
                        System.out.println("=====Bebidas=====");
                        System.out.println("Sistema de bebidas");
                        System.out.println("========================");
                        System.out.println("elija entre las opciones del 1-5");
                        System.out.println("1-Agua San Luis sin Gas Personal S/.4.90");
                        System.out.println("2-Coca Cola Sin Azúcar(1L) S/.8.90");
                        System.out.println("3-Coca Cola personal S/4.90");
                        System.out.println("4-Sprite personal S/.4.90");
                        System.out.println("5-Fanta personal S/.4.90");
                        System.out.println("6-Fanta(1L) S/.8.90");
                        System.out.println("7-Inca Kola Sin Azúcar(1L) S/.8.90");
                        System.out.println("8-Inca Kola personal S/4.90");
                        System.out.println("9-Agua Loa sin gas personal S/.3.90");
                        System.out.println("10-Sprite S/.8.90(1L)");
                        break;
                }
            case 2:
                System.out.println("=====Promociones=====");
                System.out.println("1.-Mega Promos");
                System.out.println("2.-Para Mi");
                int contiene = sc.nextInt();
                switch (contiene) {
                    case 1:
                        System.out.println("=====Mega promos=====");
                        break;
                    case 2:
                        double total = 0;
                        System.out.println("=====Para MI=====");
                        System.out.println("1.-Pizza Roll Hawaiano (S/15.90):");
                        System.out.println("2.-Pizza Roll Full Meat (S/13.90):");
                        System.out.println("3.-Pizza Roll Americano (S/12.90):");
                        System.out.println("4.-Pizza Roll Parrillero (S/15.90):");
                        System.out.println("5.-Combo Pizza Roll Hawaiana (S/16.90):");
                        System.out.println("6.-Combo Pizza Roll Meat (S/14.90):");
                        System.out.println("7.-Combo Pizza Roll Americano (S/13.90):");
                        System.out.println("8.-Combo Pizza Roll Parrillero (S/16.90):");
                        System.out.println("9.-Combo Duo Pizza Roll (S/29.90):");
                        System.out.println("10.-My Box Clasico (S/14.90):");
                        System.out.println("Selecione una opcion en (Numero): ");
                        int info = sc.nextInt();
                        switch (info) {
                            case 1:
                                total = 15.90;
                                break;
                            case 2:
                                total = 13.90;
                                break;
                            case 3:
                                total = 12.90;
                                break;
                            case 4:
                                total = 15.90;
                                break;
                            case 5:
                                total = 16.90;
                                break;
                            case 6:
                                total = 14.90;
                                break;
                            case 7:
                                total = 13.90;
                                break;
                            case 8:
                                total = 16.90;
                                break;
                            case 9:
                                total = 29.90;
                                break;
                            case 10:
                                total = 14.90;
                                break;
                            default:
                                System.out.println("Opcion invalida");
                        }
                        return total;
                }
            case 3:
                System.out.println("Redirigieno a iniciar sesion...");
                break;
            default:
                System.out.println("Opcion invalida");
        }
        return 0;
    }
}
