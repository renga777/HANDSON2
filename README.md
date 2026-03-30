# HANDSON2
HANDSON2

ATIVIDADE 1 

package handson2;


public class HandsOn2 {

    
    public static void main(String[] args) {
        
        
        System.out.println(" +\"\"\"\"\"+");
        System.out.println("[| o o |]");
        System.out.println(" |  ^  |");
        System.out.println(" | '-' |");
        System.out.println(" +-----+");
      
    }
    
    
}


ATIVIDADE 2 



package handson2_2;





public class HandsOn2_2 

{
    public static void main(String[] args) {
        double x1 = Math.toRadians(25);
        double y1 = Math.toRadians(35);
        double x2 = Math.toRadians(35.5);
        double y2 = Math.toRadians(25.5);

        double raio = 6371.01;

        double distancia = raio * Math.acos(
                Math.sin(x1) * Math.sin(x2) +
                Math.cos(x1) * Math.cos(x2) * Math.cos(y1 - y2)
        );

        System.out.println("A distância entre esses pontos é: " + distancia + " km");
    }
}



ATIVIDADE 3 


package handson2_3;
import java.util.Scanner;



public class HandsOn2_3 {
    public static void main(String[] args) {
       
        
        Scanner sc = new Scanner(System.in);

        System.out.print("Digite uma string: ");
        String texto = sc.nextLine();

        int letras = 0, numeros = 0, espacos = 0, outros = 0;

        for (int i = 0; i < texto.length(); i++) {
            char c = texto.charAt(i);

            if (Character.isLetter(c)) {
                letras++;
            } else if (Character.isDigit(c)) {
                numeros++;
            } else if (Character.isSpaceChar(c)) {
                espacos++;
            } else {
                outros++;
            }
        }

        System.out.println("Letras: " + letras);
        System.out.println("Números: " + numeros);
        System.out.println("Espaços: " + espacos);
        System.out.println("Outros caracteres: " + outros);

       
        
    }
    
}


ATIVIDADE 4 

package handson2_4;
import java.util.Scanner;


public class HandsOn2_4 {
    public static void main(String[] args) {
       Scanner sc = new Scanner(System.in);

        int tentativa = 0;
        char resposta;

        do {
            tentativa++;

            System.out.println("\nQual é o resultado de 2 + 2?");
            System.out.println("a) 3");
            System.out.println("b) 4");
            System.out.println("c) 5");
            System.out.println("d) 6");
            System.out.println("e) 7");
            System.out.print("Escolha uma opção: ");

            resposta = sc.next().toLowerCase().charAt(0);

            if (resposta == 'b') {
                System.out.println("Resposta correta na tentativa " + tentativa);
                sc.close();
                return;
            } else if (resposta == 'a' || resposta == 'c' || resposta == 'd' || resposta == 'e') {
                System.out.println("Resposta incorreta");
            } else {
                System.out.println("Opção inválida");
                tentativa--; 
            }

        } while (tentativa < 3);

        System.out.println("Resposta incorreta nas 3 tentativas");
    }
}


