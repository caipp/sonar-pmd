# UselessQualifiedThis
**Category:** `pmd`<br/>
**Rule Key:** `pmd:UselessQualifiedThis`<br/>


-----

<p>Look for qualified this usages in the same class.</p>

<p>Examples:</p>

<pre>
public class Foo {
  final Foo otherFoo = Foo.this;  // use "this" directly

  public void doSomething() {
    final Foo anotherFoo = Foo.this;  // use "this" directly
  }

  private ActionListener returnListener() {
    return new ActionListener() {
      @Override
      public void actionPerformed(ActionEvent e) {
        doSomethingWithQualifiedThis(Foo.this);  // This is fine
      }
    };
  }

  private class Foo3 {
    final Foo myFoo = Foo.this;  // This is fine
  }

  private class Foo2 {
    final Foo2 myFoo2 = Foo2.this;  // Use "this" direclty
  }
}
</pre>
