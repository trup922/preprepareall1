# 1. Java Programs

## Reverse number

```
public static void main(String[] args) {
		int no = 4587;
		int rev = 0;

		while (no > 0) {
			int right = no % 10; // take right most number i.e 7 from 4587
			rev = rev * 10 + right; // multiply rev* 10 and add right most number
			no = no / 10; // skip right most number by dividing by 10 -- 4587/10 -- 458
		}

		System.out.println(rev);
	}
```

## Reverse String

```
	public static void main(String[] args) {
		String str="tushar";
		StringBuilder strb=new StringBuilder();
		for(int i=str.length()-1;i>=0;i--) {
			strb.append(str.charAt(i));
		}
		System.out.println(strb.toString());
	}
```

## Fibonaci

```
public static void main(String[] args) {
	int n1=0,n2=1,n3, count=11;
	System.out.print(" "+n1);
	for(int i=2;i<count;i++) {
		n3=n2+n1; 
		n1=n2;
		n2=n3;
		System.out.print(" "+n3);
	}
}
```

## Factorial number

```
public static void main(String[] args) {
		int num = 4;
		int fact = 1;
		while (num > 0) {
			fact = fact * num;
			num--;
		}
		System.out.println(fact);
	}
```

## Armstrong number

```
	public static void main(String[] args) {
		int num = 371;
		int actualnumber=num;
		int right, add = 0;

		while (num > 0) {
			right = num % 10;
			add = add + (right * right * right);
			num = num / 10;
		}

		System.out.println(actualnumber == add ? "true" : "false");

	}
```

## Prime number

```
public static void main(String[] args) {
		int no = 5;
		boolean flag = true;
		for (int i = 2; i < no / 2; i++) {
			if (no % i == 0) { // divide actual number by i
				flag = false;
				break;
			}
		}
		System.out.println(flag == true ? "Prime number" : "Not a prime number");
	}
```

## Largest number, second , third

```
public static void main(String[] args) {
		int arr[]= {13,4,82,49,23,45,81};
		int temp;
		for(int i=0;i<arr.length-1;i++) {
			for(int j=i+1;j<arr.length-1;j++) {
				if(arr[i]<arr[j]) {
					temp=arr[i];
					arr[i]=arr[j];
					arr[j]=temp;
				}
			}
		}
		
		System.out.println(Arrays.toString(arr));
		System.out.println("second largest "+arr[1]);
			
	}
```

## Palindrome number

```
public static void main(String[] args) {
		String str = "level";
		int start = 0;
		int end = str.length() - 1;
		boolean flag = true;
		while (start < end) {
			if (str.charAt(start) != str.charAt(end)) {
				flag = false;
				break;
			}
			start++;
			end--;
		}

		System.out.println("is palindrome? " + flag);

	
```
