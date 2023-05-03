Download Link: https://assignmentchef.com/product/solved-cs307-project-2
<br>
<h1>Interface Specification</h1>

We provide the interfaces code in two language (Java, Python). You can use either of them upon your preference. Notice

that due to the inherent differences between these two language, the <strong>Score Policy</strong> may also be different.

The structure of the interfaces is as follows. database folder stores connection information such as username, password, url, we only

provides PostgreSQL as the DBMS.

dto folder stores a set of data objects that will be accessed by interfaces. Your

implementation will use them as parameters or returned values.

service folder stores <strong>Service Interfaces</strong>, this is the folder you should pay special attention

<ol>

 <li>There exist multiple .java file where the interface signatures are stored. You need to implement you own class to fit these signatures.</li>

</ol>

exception folder stores exceptions that you should throw if something went wrong. factory folder stores the ServiceFactory abstract class that you need to implement to

create your service instances.

<h1>Your Tasks</h1>

Implement the service and factory interfaces to pass the base testcases.

Design your (PostgreSQL) database to satisfy the requirements of interfaces.

Profile your implementation and find ways to speed it up.

(Optional) Find other ways to implement similar functionalities as our interfaces and compare (some of) them, are they better, worse or have different use cases.

Here is a reference implementation, it shows you how to implement one method of an interface.

To get a service working, you’ll have to implement <strong>all its interfaces</strong>

<em>The following code is just a guide, the code interacts with database will usually be written in the DAO layer</em>

<h1>Additional requirements of interface</h1>

<h2>Java</h2>

All add*() functions with int as return value should return the (presumably auto-generated) ID.

All arguments are guaranteed to be non-null, unless marked as @Nullable. All return values (and their fields) should be non-null, unless explicitly documented otherwise. If a list/map is empty, put List.of()/Map.of() or equivalents instead of null.

Do <strong>NOT</strong> modify anything in the provided interfaces, or any of the framework code. Your implementation should throw java.lang.UnsupportedOperationException if a method is not actually implemented, so the tests can fail quickly.

<h2>Python</h2>

All add*() functions with return value of int should return the (presumably auto-generated) ID.

All arguments are guaranteed to follow the type hints. Arguments passed won’t be None unless explicitly annotated with Optional .

For return types with type hints, return values (and their fields) should not be None , unless explicitly documented.

Use [] , {} , set() or their equivalents instead of None for empty container in return values.

Your implementation should raise NotImplementedError if a method is not actually implemented, so that tests can fail quickly.

<h1>Rules</h1>

Data should be persisted on disk after each write operation instead of only modified in RAM. If you introduced a cache layer, you have to enforce the consistency. You should also ensure the durability in case of a sudden shutdown.

You should <strong>NOT</strong> use frameworks such as <strong>ORM</strong>.

You don’t need to spend time on <strong>GUI/WEB</strong>, as we do <strong>NOT</strong> give extra scores for them.

<h2>Java-specific rules</h2>

You should <strong>NOT</strong> modify or add any class in package cn.edu.sustech.cs307 . Use another package for your implementations.

You should <strong>NOT</strong> extend any class in package cn.edu.sustech.cs307.dto .

In this project, we use Maven to manage dependent libraries. If you want to introduce a new library, you need to record it in pom.xml . Your dependencies should be downloadable from the Maven Central repository.