# calculator
import org.junit.Test;
        import org.junit.runner.RunWith;
        import org.junit.runners.Parameterized;
        import org.junit.runners.Parameterized.Parameters;

        import java.util.Arrays;
        import java.util.Collection;

@RunWith(Parameterized.class)
public class CalculatorTest {
    // Student information:
    // Student id:B221202372
    // Name: SADIK MERT
    // Surname: DİNCEL
    // Course name: software verification and validation
    // Homework1
    // Repository address: https://github.com/mrt6060

    private int number1;
    private int number2;
    private int Sum;

    public CalculatorTest(int number1, int number2, int Sum) {
        this.number1 = number1;
        this.number2 = number2;
        this.Sum = Sum;
    }

    @Parameters
    public static Collection<Object[]> data() {
        return Arrays.asList(new Object[][] {
                { 6, 2, 5 },  // num1, num2, expectedSum
                { -5, 7, 1 },
                { 5, 4, 0 },
                { -2, -3, -7 },
                
        });
    }

    @Test
    public void testAddition() {
        Calculator calculator = new Calculator();
        int result = calculator.add(number1, number2);
        assertEquals(Sum, result);
    }

    
}
