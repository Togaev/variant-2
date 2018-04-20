import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

/**
 * Created by Mikhail on 20.04.2018.
 */
 
 
public class VaiantIndex {

    public static void main(String[] args) throws Exception {
        int[] array = initializeArray();

        int max = max(array);
        System.out.println(max);
    }

    public static int[] initializeArray() throws IOException {
        //создаем массив и вводим данные
        int[] array = new int[5];

        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        for (int i = 0; i < array.length; i++)
            array[i] = Integer.parseInt(reader.readLine());


        return array;
    }

    public static int max(int[] arr) {

        int maxindex = 0;
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] > arr[maxindex]) {
                maxindex = i;
            }
        }
        return maxindex;
    }
}
