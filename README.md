# stockmax_hacker_rank
It is hacker rank question. It is stock_max question

package Medium_Module;

import java.util.Scanner;

import Checking_Class.LinkedList;

public class stockmax {
	
	public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);
		
		int n = sc.nextInt();
		for(int i = 0 ; i < n ; i++)
		{
			int m = sc.nextInt();
			int price[] = new int[m];
			for(int j = 0 ; j < m ; j++)
			{
				price[j] = sc.nextInt();
			}
			System.out.println(maxProfit(price));	
		}
	}
	public static long maxProfit(int[] price)
	{
		long profit = 0L;
		int maxsofar = 0;
		for(int i = price.length - 1 ; i > -1 ; i--)
		{
			if(price[i] >= maxsofar)
			{
				maxsofar = price[i];
			}
			profit = profit + maxsofar - price[i];
		}
		return profit;
	}

}

