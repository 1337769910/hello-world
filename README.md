# hello-world
Just a repository
package patpractice;

//import java.math.BigInteger;
import java.util.ArrayList;
import java.util.Scanner;

public class practice11 {
public static void main(String[] args) {
	Scanner s =new Scanner(System.in);
	ArrayList<Num> al = new ArrayList<Num>();
	for(int i =0;i<10;i++) {
	al.add(new Num(i,0));
	}
	String a =s.nextLine();
	int A =Integer.parseInt(a);
	int[] bit =new int[a.length()];
//	BigInteger A =s.nextBigInteger();
	for(int i =0;i<a.length();i++){
		bit[i]=A%10;
		A=A/10;
//		bit[i]=A.divide(10);
		
	}
	for(int i=0;i<bit.length;i++) {
		if(bit[i]==0) {
			al.get(bit[i]).M++;
		}
	}
	
for(int i=0;i<10;i++) {
	if(al.get(i).M!=0) {
		System.out.println(al.get(i).D+":"+al.get(i).M);
	}
}
}
public static class Num{
	int D ;
	int M ;
	public Num(int D,int M) {
		this.D =D;
		this.M =M;
	}
}

	

}
