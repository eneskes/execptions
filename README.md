# execptions
import java.io.FileInputStream;
import java.io.FileNotFoundException;
import java.io.IOException;
public class C01_FileInputStream {
    public static void main(String[] args) {
        String dosyaYolu="src/day40_exceptions/dosya";
        try {
            FileInputStream fis=new FileInputStream(dosyaYolu);
            int k=0;
            while( (k=fis.read())!=-1){
                System.out.print((char)k);
            }
        } catch (FileNotFoundException e) { // FileNotFoundException
            e.printStackTrace();
        }  catch (IOException e) { // IOException
            e.printStackTrace();
        }
