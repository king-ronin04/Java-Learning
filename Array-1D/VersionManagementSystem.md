# Version Management System

A version Managementsystem (VMS) is a repository of files, often the files for the source code of computer programs, with monitored access. Every change made to the source is tracked, along with who made the change, why they made it, and references to problems fixed, or enhancements introduced, by the change.
<br>
In this problem we will consider a simplified model of a development project. Let's suppose that there are N source files in the project. All the source files are distinct and numbered from 1 to N.

A VMS which is used for maintaining the project contains two sequences of source files. The first sequence contains M source files that are ignored by the VMS. If a source file is not in the first sequence, then it's considered to be unignored. The second sequence contains K source files that are tracked by the VMS. If a source file is not in the second sequence, then it's considered to be untracked.

A source file can either be or not be in any of these two sequences. Your task is to calculate two values: the number of source files of the project, that are both tracked and ignored, and the number of source files of the project, that are both untracked and unignored.

#### Input format :
The first line of the input contains three integers N, M and K denoting the number of source files in the project, the number of ignored source files and the number of tracked source files. Assume that the maximum value for N as 50.
<br>
The second line contains M distinct integers denoting the sequence A of ignored source files. The sequence is strictly increasing.
<br>
The third line contains K distinct integers denoting the sequence B of tracked source files. The sequence is strictly increasing.

#### Output format :
Output a single line containing two integers: the number of the source files, that are both tracked and ignored, and the number of the source files, that are both untracked and unignored.

**Sample test cases :<br>
Input 1 :**
```
7 4 6
1 4 6 7
1 2 3 4 6 7
```
**Output 1 :**
```
4 1
```
**Input 2 :**
```
4 2 2
1 4
3 4
```
**Output 2 :**
```
1 1
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------


```java
import java.io.*;
import java.util.*;
class Versionmanagementsystem {
	public static void main(String [] args) {
		int i,j,n,m,k,l,c=0,cc=0;
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		m = sc.nextInt();
		k = sc.nextInt();
		int a[] = new int[m];
		int b[] = new int[k];
		for(i=0;i<m;i++) {
			a[i] = sc.nextInt();
		}
		for(i=0;i<k;i++) {
			b[i] = sc.nextInt();
		}
	    for(i=0;i<m;i++)
	    {
	        for(j=0;j<k;j++)
	        {
	            if(a[i]==b[j]){c++;}
	        }
	    }
	    for(i=1;i<=n;i++)
	    {
	        for(j=0;j<m;j++)
	        {
	            if(a[j]==i)
	            {
	                break;
	            }
	            if(j==m-1)
	            {
	                for(l=0;l<k;l++)
	                {
	                    if(b[l]==i)
	                    {
	                        break;
	                    }
	                    if(l==k-1){cc++;}
	                }
	            }
	        }
	    }
	    System.out.println(c+" "+cc);

	}
}

```





