
## Complete Code Example


### /SpringbootPracticewithJpas/git/getting-started-in-5-steps/junit-in-5-steps/src/com/SpringbootPracticewithJpas/junit/MyMath.java

```java
package com.SpringbootPracticewithJpas.junit;

public class MyMath {
	int sum(int[] numbers) {
		int sum = 0;
		for (int i : numbers) {
			sum += i;
		}
		return sum;
	}
}
```
---

### /SpringbootPracticewithJpas/git/getting-started-in-5-steps/junit-in-5-steps/test/com/SpringbootPracticewithJpas/junit/AssertTest.java

```java
package com.SpringbootPracticewithJpas.junit;

import static org.junit.Assert.assertEquals;
import static org.junit.Assert.assertTrue;

import org.junit.Test;

public class AssertTest {

	@Test
	public void test() {
		boolean condn = true;
		assertEquals(true, condn);
		assertTrue(condn);
		// assertFalse(condn);
	}

}
```
---

### /SpringbootPracticewithJpas/git/getting-started-in-5-steps/junit-in-5-steps/test/com/SpringbootPracticewithJpas/junit/MyMathTest.java

```java
package com.SpringbootPracticewithJpas.junit;

import static org.junit.Assert.assertEquals;

import org.junit.After;
import org.junit.AfterClass;
import org.junit.Before;
import org.junit.BeforeClass;
import org.junit.Test;

public class MyMathTest {
	MyMath myMath = new MyMath();

	@Before
	public void before() {
		System.out.println("Before");
	}

	@After
	public void after() {
		System.out.println("After");
	}

	@BeforeClass
	public static void beforeClass() {
		System.out.println("Before Class");
	}

	@AfterClass
	public static void afterClass() {
		System.out.println("After Class");
	}

	// MyMath.sum
	// 1,2,3 => 6
	@Test
	public void sum_with3numbers() {
		System.out.println("Test1");
		assertEquals(6, myMath.sum(new int[] { 1, 2, 3 }));
	}

	@Test
	public void sum_with1number() {
		System.out.println("Test2");
		assertEquals(3, myMath.sum(new int[] { 3 }));
	}
}
```
---
