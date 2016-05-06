import java.util.Arrays;
import java.util.List;
import java.util.Scanner;
import java.util.stream.Collectors;

public class FilterArray {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        List<String> line = Arrays.asList(sc.nextLine()
                .split("\\W+"))
                .stream()
                .filter(a -> a.length() > 3)
                .collect(Collectors.toList());
        if (line.isEmpty()) {
            System.out.print("(empty)");
        } else {
            line.forEach(e -> System.out.print(e + " "));
        }
    }
}
