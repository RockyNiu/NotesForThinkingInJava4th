# NotesForThinkingInJava4th
Notes for Thinking In Java(4th) by Bruce Eckel

Not every Java Developer, especially who is switching or switched from other fields/professions, have read the book Thinking In Java words by words. However, I bet, the best ones do.

Here is my plan: 25~50 pages a day (around 2~5 hours) , finish it in six weeks.
* Inner Classes took me three days.

<table>
  <tr>
    <th>Day</th>
    <th>Pages</th>
    <th>Difficulty</th>
    <th>Notes</th>
  </tr>
  <tr>
    <td>00</td>
    <td>0 - 60</td>
    <td>**</td>
    <td>Skip jsp and applet</td>
  </tr>
  <tr>
    <td>01</td>
    <td>61 - 92</td>
    <td>**</td>
    <td>Passing object reference by value. Practically skip "static import" ?</td>
  </tr>
  <tr>
    <td>02</td>
    <td>93 - 154</td>
    <td>*</td>
    <td>Boolean is special. Switch is updated in Java7</td>
  </tr>
  <tr>
    <td>03</td>
    <td>155 - 181</td>
    <td>***</td>
    <td>Garbage collection: stop-and-copy, mark-and-sweep
    </td>
  </tr>
  <tr>
    <td>04</td>
    <td>182 - 236</td>
    <td>***</td>
    <td>Initialization and creation:  一个类是先初始化static的变量和static句块，
    然后再分配该类以及父类的成员变量的内存空间，赋予默认值，然后开始调用构造函数。
    而子类和父类之间，则先初始化和创建父类，然后再初始化和创建子类的。
    Access control: 
    public, protected, (default), private
    </td>
  </tr>
  <tr>
    <td>05</td>
    <td>237 - 276</td>
    <td>**</td>
    <td>Subclasses do not inherit private fields.
    is-a: inheritance, has-a: composition.
    final: fields, arguments, methods, classes.
    </td>
  </tr>
  <tr>
    <td>06</td>
    <td>277 - 310</td>
    <td>***</td>
    <td>
    Reference counting: good for mobile app to show synchronization icon. 
    The only safe methods to call inside a constructor are those that are final in the base class.
    Composition first: use inheritance to express differences in behavior, and fields to express variations in state.
    </td>
  </tr>
  <tr>
    <td>07</td>
    <td>311 - 344</td>
    <td>**</td>
    <td>Strategy Pattern/Factory Pattern. 
    Any abstraction should be motivated by a real need. 
    An appropriate guideline is to perfer classes to interfaces.
    </td>
  </tr>
  <tr>
    <td>08-10</td>
    <td>345 - 388</td>
    <td>****</td>
    <td>Anonymous inner class: requires the agument reference, which is object and outside, be final; can either extend a class or implement an interface, but not both.
    Nested class: static.
    Template Method design pattern.
    </td>
  </tr>
  <tr>
    <td>11-12</td>
    <td>389 - 442</td>
    <td>**</td>
    <td>Stack: not good in Java. Queue: concurrency.
    </td>
  </tr>
</table>
