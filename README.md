# Last-Digit-Checker
This program returns true if at least two of the numbers share the same rightmost digit, otherwise, it should return false.

public class LastDigitChecker {

    public static void main(String[] args) {
        System.out.println(hasSameLastDigit(23, 32, 42));
        System.out.println(isValid(20));
    }

    public static boolean hasSameLastDigit(int x, int y, int z) {

        if(isValid(x) && isValid(y) && isValid(z)) {


            int xLastDigit = x % 10;
            int yLastDigit = y % 10;
            int zLastDigit = z % 10;

            return (xLastDigit == yLastDigit || xLastDigit == zLastDigit || yLastDigit == zLastDigit);
        }
        return false;
    }

    public static boolean isValid(int check) {
        return check >= 10 && check <= 1000;

    }
}

