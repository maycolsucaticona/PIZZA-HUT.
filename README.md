import java.util.Scanner;

    public static void main(String[] args){
        Scanner escaner=new Scanner(System.in);
        boolean estado=false;
        String DNI, contraseña;
        int intento=3;
        double meta=0;
        double saldo=0;
        int opcion;
        while(estado==false&&intento>0){
            System.out.println("BIENVENDIO A TU ALCANCIA MAS VONOCIDA COMO PORQUI AHORRADOR");
            System.out.println(" ingrese su DNI");
            DNI= escaner.nextLine();
            System.out.println("ingrese su contraseña");
            contraseña= escaner.nextLine();
            if(DNI.equals("123")&&contraseña.equals("123")){
                System.out.println("SESION INICIADA");
                estado=true;
            }
            else{
                System.out.println("Acceso denegado. Intente de nuevo");
                intento++;
                System.out.println("cantidad de intentos restantes"+intento);
            }
        }
        if(intento==0){
            System.out.println("cuenta bloqueada por 24 horas ");
        }
        if (estado==true){
            System.out.println("ingrese la cantidad de soles a ahorrar");
            meta= escaner.nextDouble();
            while (estado==true){
                System.out.println("selecione entre las siquientes opciones ");
                System.out.println("1: consultar saldo");
                System.out.println("2: depositar dinero");
                System.out.println("3: retirar dinero");
                System.out.println("4: salir");
                opcion= escaner.nextInt();
                switch (opcion){
                    case 1:
                        System.out.println("su saldo disponible es"+saldo);
                        break;
                    case 2:
                        System.out.println("ingrese la cantidad a depositar");
                        double deposito= escaner.nextDouble();
                        if(deposito>=1){
                            saldo=saldo+deposito;
                            System.out.println("su saldo actual es"+saldo);
                            if(saldo>meta){
                                System.out.println("Felicitaciones superaste la meta  ahorrar");
                            }
                        }
                        else{
                            System.out.println("no se puede depositar saldos menores a S/1.00");
                        }
                        break;
                    case 3:
                        System.out.println("ingrese la cantidad a depositar");
                        double retiro= escaner.nextDouble();
                        if(retiro==saldo){
                            saldo=saldo-retiro;
                            double faltante=meta-saldo;
                            System.out.println("su saldo actual es"+saldo);
                            System.out.println("tu puedes, falta"+faltante+"para llegar a la meta ");
                        }
                        else{
                            System.out.println("el retiro debe ser menor o igual a su saldo disponible");
                        }
                        break;
                }
            }
        }
    }
}
