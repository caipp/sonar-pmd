# BeanMembersShouldSerialize
**Category:** `pmd`<br/>
**Rule Key:** `pmd:BeanMembersShouldSerialize`<br/>


-----

If a class is a bean, or is referenced by a bean directly or indirectly it needs to be serializable. Member variables need to be marked as transient, static, or have accessor methods in the class. Marking variables as transient is the safest and easiest modification. Accessor methods should follow the Java naming conventions, i.e.if you have a variable foo, you should provide getFoo and setFoo methods.
