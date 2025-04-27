# AP-assignment-4th-
Create a class calculator with a method add (int a, int b). Write a unit test to verify the result
public class Calculator {
    public int add(int a, int b) {
        return a + b;
    }
}
import static org.junit.jupiter.api.Assertions.assertEquals;
import org.junit.jupiter.api.Test;

public class CalculatorTest {

    @Test
    public void testAdd() {
        Calculator calculator = new Calculator();
        int result = calculator.add(5, 3);
        assertEquals(8, result, "5 + 3 should equal 8");

        result = calculator.add(-1, 1);
        assertEquals(0, result, "-1 + 1 should equal 0");

        result = calculator.add(0, 0);
        assertEquals(0, result, "0 + 0 should equal 0");

        result = calculator.add(-5, -3);
        assertEquals(-8, result, "-5 + -3 should equal -8");
    }
}
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter</artifactId>
    <version>5.8.1</version>
    <scope>test</scope>
</dependency>
