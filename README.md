# NotesForThinkingInJava4th
Notes for Thinking In Java(4th) by Bruce Eckel

Not every Java Developer, especially who is switching or switched from other fields/professions, have read the book Thinking In Java words by words. However, I bet, the best ones do.

Here is my plan: 25~50 pages a day (around 2~5 hours) , finish it in six weeks (may double the time?)

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
    <td>Stack: not good in Java. Queue: concurrency. Iterable: foreach. Adapter Method. Pay attention to Arrays.asList().
    </td>
  </tr>
  <tr>
    <td>13-15</td>
    <td>443 - 502</td>
    <td>***</td>
    <td>RuntimeException: cannot be anticipated, or have been checked. Finally: return; lost exception pitfall. Exception Guidelines at p500.
    </td>
  </tr>
  <tr>
    <td>16-17</td>
    <td>503 - 552</td>
    <td>****</td>
    <td>javap -c. CharSequence: CharBuffer, String, StringBuffer, StringBuilder. Regular expression (refer to "Mastering Regular Expressions"): Scanners, exmaples in p542 and p550.
    </td>
  </tr>
  <tr>
    <td>18-20</td>
    <td>553 - 616</td>
    <td>****</td>
    <td>RTTI: Runtime Type Inforamtion; Loading->Linking->Initialization; Class.forName(): init vs *.class: not init (except constant); instanceof, isInstance, isAssignableFrom, derived; ?? InvocationHandler, Proxy.newProxyInstance, Null Object; Field setAccessbile(true): by reflection, touch every things.
    </td>
  </tr>
  <tr>
    <td>21-27</td>
    <td>Break</td>
    <td></td>
    <td>Happy Chinese New Year!
    </td>
  </tr>
  <tr>
    <td>59-64</td>
    <td>617-746</td>
    <td>****</td>
    <td>Tuple, Data Transfer Object(Messenger, p621), the recipient of the object is allowed to read the elements but not put new ones in; Generic Interfaces: Generator<T>; Generic Method: type argument inference, Explicit type specification when not an assignment statment; Erasure: there is no information about generic parameter types available inside generic code; the cause: corpoorating the packages with generified codes and those without generified codes; Array.newInstance(): creating arrays in generics anything that requires the knowledge of exact type at run time won't work; When you discover you can ignore warnings, you do; Bounds; Wildcards; <? super Clas>: supertype bounds relax the constraints on what you can pass into a method; List: "a raw List that holds any Object type", List<?>: "a non-raw List of some specific type, but we just don't know what that type is"; capture conversion; Self-bounded types: if you use self-bounding, you only end up with one version of a method, which takes the exact argument type; Curiously Recurring Generics; Dynamic type safety: Collections.checkedList()... ; Mixins with dynamic proxies; Duck typing: if it walks like a duck and talks like a duck, you might as well treat it like a duck; 
    </td>
  </tr>
    <tr>
    <td>28-58</td>
    <td>1109-1302</td>
    <td>*****</td>
    <td>Functional language, task safe; executor; CachedThreadPool, FixedThreadPool, SingleThreadExecutor, Callable, Executor, Service.submit(); TimeUnit.milliSecond.sleep(), Set priority in run, yield is an hint; deamon, threadmethod, t.join(), t.getUncaughtExceptionHandler, t.getDefaultUncaghtException;Race Condition, Mutex; Increment is not safe, synchronized method need private field; Atomicity, Volatility; AtomicInteger, AtomicLong, AtomicReference; Critical Section, Synchronized block to allow other tasks more access, Collections.SynchronizedList; instanceOf, isInstance, isAssignableFrom, derived InvocationHandler; Thread local storage, new Runnable blocked dead, interrupt interrupted, shutDownNow cancel, Execute shutdownnow, nio for io; sleep/yield does not release the lock, wait release; wait() belongs to object, should be put in synchronized method or block, otherwise IllegalMonitorStateException; Always surround wait() with while loop: synchronized (sharedMonitor){while(conditionIsNotMet){sharedMonitor.wait();}}; Lock and condition/await()/signal(),signalAll() only necessary for more difficult threading problems; Producers and Consumers Model; BlockingQueue, LinkedBlockingQueue, ArrayBlockingQueue; Blocking Queue, PipedWriter, PipedReader; shutDownNow will not interrupt system.in.read. Preventing deadlock through careful program design is a critical part of developing concurrent; Four Conditins for dead lock; CountDownLatch, CyclicBarrier; DelayQueue; Delayed, getDealy(TimeUnit), implements Comparable; PriorityBlockingQueue; ScheduledExecutor,; ScheduledThreadPoolExecutor; Semaphore; Exchanger; Simulation, Bank teller simulation, the restaurant simulation, distributing work; In complex concurrenty situation, Lock is faster than synchronized(p1280); CopyOnWriteArrayList, CopyOnWriteArraySet, ConcurrentHashMap, ConcurrentLinkedQueue; ReentrantReaderWriterLock; Active Objects(p1298), agent-based programming. </td>
  </tr>
</table>
</table>
