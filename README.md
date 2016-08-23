public class PerfectNumber {

	/**
	 * 完全数
	 * 完数就是它的所有（余数为0的）被除数相加的和等于它本身（其中的被除数要除去它本身）
	 */
	
	public static boolean isPerfectNumber(int n){
		int sum = 0;
		for(int i=1;i<=n/2;i++)
			if(n%i==0)
				sum += i;
		if(sum==n)
			return true;
		return false;
	}
	
	public static void main(String[] args) {
		System.out.println(isPerfectNumber(6));
		for(int a=1;a<=1000;a++){
			int sum=0;
			for(int i=1;i<=a/2;i++)
				if(a%i==0)
					sum+=i;
			if(a==sum)
				System.out.println(a);
		} 
	}
	
}
