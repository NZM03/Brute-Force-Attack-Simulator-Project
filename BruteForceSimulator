import java.util.Scanner;
import java.util.concurrent.TimeUnit;

public class BruteForceSimulator {

    // Simulated password
    private static final String PASSWORD = "secure123";

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Starting brute force password simulation...");

        // Generate possible passwords (only for demo; not exhaustive for simplicity)
        char[] charset = "abcdefghijklmnopqrstuvwxyz0123456789".toCharArray();
        bruteForce(charset);
    }

    private static void bruteForce(char[] charset) {
        long startTime = System.currentTimeMillis();
        int maxLength = 8;  // Limit password length for simplicity
        String result = null;

        outerLoop:
        for (int length = 1; length <= maxLength; length++) {
            char[] current = new char[length];
            if (attemptPassword(charset, current, 0)) {
                result = new String(current);
                break outerLoop;
            }
        }

        long endTime = System.currentTimeMillis();
        if (result != null) {
            System.out.println("Password found: " + result);
        } else {
            System.out.println("Password not found within the length limit.");
        }
        System.out.println("Time taken: " + (endTime - startTime) + " ms");
    }

    private static boolean attemptPassword(char[] charset, char[] current, int position) {
        if (position == current.length) {
            String attempt = new String(current);
            System.out.println("Attempting: " + attempt);
            try {
                TimeUnit.MILLISECONDS.sleep(100);  // Simulate delay for each attempt
            } catch (InterruptedException e) {
                Thread.currentThread().interrupt();
            }
            return attempt.equals(PASSWORD);
        }

        for (char c : charset) {
            current[position] = c;
            if (attemptPassword(charset, current, position + 1)) {
                return true;
            }
        }
        return false;
    }
}
