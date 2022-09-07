# Practice Binary Search



public class BinarySearch {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		//it works on the sorted arrays
		int[] arr= {1,2,3,45,89,789,908};
		
		int target=908;
		
		int  ans=isPresent(arr,target);
		System.out.println(ans);
	}
		
	static int  isPresent(int[] arr,int target) {
			
			int start=0;int end=arr.length-1;
		while(start<=end) {
			//int middle=(start+end)/2;//some times the integers range may exceeds when we apply start +end /2 to avoid this 
			//we gonna use  int middle=start +(end-start)/2;
			int middle=start +(end-start)/2;
			if(target==arr[middle]) {
				return middle;
	
			}
			if(target>arr[middle]) {
				start=middle+1;
	
			}
			else {
				end=middle-1;
		
			}
			
		}
		return -1;
		

	}
	
	}
