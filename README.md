# com.gmail.julechka.shevchuk

public class Fibonacci {

    private static final int MAX_VALUE = 4000000;

    private static int sum(int firstNumber, int secondNumber, int sum) {
        sum += secondNumber % 2 == 0 ? secondNumber : 0;
        if (secondNumber > MAX_VALUE) {
            return sum;
        }
        return sum(secondNumber, firstNumber + secondNumber, sum);
    }

    public static int sum() {
        return sum(1, 2, 0);
    }


    public static void main(String[] args) {
        System.out.println(Fibonacci.sum());
    }

}
