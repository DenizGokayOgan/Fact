# Fact
  import java.util.Scanner;

  public class Main {
    public static void main(String[] args) {
        int n,r,nFak=1,rFak=1,mines=1,c;
        int i;
        Scanner input = new Scanner(System.in);
        System.out.println("n'in r'li kombinasyonu için");
        System.out.print("n sayısı giriniz: ");
        n = input.nextInt();
        System.out.print("r sayısı giriniz :");
        r = input.nextInt();
        for(i=1 ; i<=n; i++){
            nFak = i*nFak;
        }
        for(i=1 ; i<=r; i++){
            rFak = i*rFak;
        }
        int s= n-r;
        for(i=1 ; i<=s; i++){
            mines = i*mines;
        }
        c = (nFak) / (rFak * mines);
        System.out.println("C(n,r) = " +c);
    }
}
