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
                break;

            case 2:
                registrarse();
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
    public static void registrarse(){
        Scanner sc = new Scanner(System.in);
        System.out.println("=====REGISTRO=====");
        System.out.println("Ingrese su Nombre:");
        String nombre = sc.nextLine();
        System.out.println("Ingrese Apellido:");
        String apellido = sc.nextLine();
        System.out.println("Ingrese su N°de celular:");
        int celular = sc.nextInt();
        System.out.println("Ingrese su DNI");
        int dni = sc.nextInt();

        System.out.println("===DATOS REGISTRADOS===");
        System.out.println("Nombre:"+nombre);
        System.out.println("Apellido:"+apellido);
        System.out.println("Celular:"+celular);
        System.out.println("DNI:"+dni);
    }
}
