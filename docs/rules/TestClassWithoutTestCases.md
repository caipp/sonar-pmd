# TestClassWithoutTestCases
**Category:** `pmd-unit-tests`<br/>
**Rule Key:** `pmd-unit-tests:TestClassWithoutTestCases`<br/>


-----

Test classes end with the suffix Test. Having a non-test class with that name is not a good practice, since most people will assume it is a test case. Test classes have test methods named testXXX.
Beware: This rule doesn't support JUnit 4.x's @Test annotation.
<pre>
public class CarTest { // violation, consider changing the name of the class if it is not a test
  // consider adding test methods if it is a test
  public static void main(String[] args) {
    // do something
  }
}
</pre>
