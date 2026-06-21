import java.util.Scanner;

public class CaesarCipher {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("Caesar Cipher");
        System.out.println("1. Encrypt");
        System.out.println("2. Decrypt (try all shifts)");
        System.out.print("Enter 1 or 2: ");
        int choice = sc.nextInt();
        sc.nextLine();

        if (choice == 1) {
            System.out.print("Enter message: ");
            String message = sc.nextLine();
            System.out.print("Enter key (1-25): ");
            int key = sc.nextInt();

            String result = "";
            for (int i = 0; i < message.length(); i++) {
                char c = message.charAt(i);
                if (Character.isLetter(c)) {
                    char base = Character.isLowerCase(c) ? 'a' : 'A';
                    char newChar = (char) ((c - base + key) % 26 + base);
                    result = result + newChar;
                } else {
                    result = result + c;
                }
            }
            System.out.println("Encrypted message: " + result);

        } else if (choice == 2) {
            System.out.print("Enter encrypted message: ");
            String message = sc.nextLine();
            System.out.println("Trying all possible shifts:");

            for (int key = 1; key <= 25; key++) {
                String result = "";
                for (int i = 0; i < message.length(); i++) {
                    char c = message.charAt(i);
                    if (Character.isLetter(c)) {
                        char base = Character.isLowerCase(c) ? 'a' : 'A';
                        char newChar = (char) (((c - base - key) % 26 + 26) % 26 + base);
                        result = result + newChar;
                    } else {
                        result = result + c;
                    }
                }
                System.out.println("Shift " + key + " : " + result);
            }

        } else {
            System.out.println("Invalid choice");
        }

        sc.close();
    }
}
