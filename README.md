# Counting-Duplicate-Characters
public class CP2 {

    static final int NO_OF_CHARS = 256;
    static void countDuplicateChar(String str,
    int[] count)
    {
        for (int i = 0; i < str.length(); i++)
            count[str.charAt(i)]++;
    }
    static void printDuplicateChar(String str)
    {
        int count[] = new int[NO_OF_CHARS];
        countDuplicateChar(str, count);
 
        for (int i = 0; i < NO_OF_CHARS; i++)
            if (count[i] > 1)
                System.out.println((char)(i) +
                          ", count = " + count[i]);
    }

    public static void main(String[] args)
    {
        String str = "computerprogramming";
        printDuplicateChar(str);
    }
}
