
# 入口点

JavaProjectBuilder 是 QDox 的入口点。它负责解析源代码、解析导入和存储数据。

要创建它，只需调用默认构造函数即可。

```java
JavaProjectBuilder builder = new JavaProjectBuilder();
```

## 读取源文件

Java 源代码可以添加到 JavaProjectBuilder 中。源代码可以一次读取一个文件（使用 java.io.Reader），也可以递归添加整个源代码树。


```java
// 读取单个源文件
builder.addSource(new FileReader("MyFile.java"));

// 从输入流读取数据
builder.addSource(new StringReader("package test; public class Hello {}"));

// 添加源代码树中的所有 .java 文件（递归）
builder.addSourceTree(new File("mysrcdir"));
```


# 解析类名

为了解析使用通配符（例如 import java.util.*;）导入的类，ClassLibrary 必须了解项目中使用的其他类。  
  
ClassLibrary 有 4 种解析类的方法：  
  
* 查看已添加的其他源。  
* 通过搜索提供的源文件夹  
* 在当前 classpath（包括标准 JRE 类）中查找。  
* 查看运行时指定的其他 ClassLoaders。  
  
所有添加到 JavaProjectBuilder 的源和源代码都将被解析。这往往远远超出了需要。为提高效率，可使用 ClassLibrary 添加源文件夹。将这些文件视为懒解析源。  
  
JavaProjectBuilder 会自动设置当前的 classpath。在大多数情况下，这就足够了，但在某些情况下，您可能希望在外部库中解析完整的类。

```java
// Get the ClassLibrary
JavaProjectBuilder builder = new JavaProjectBuilder();

// Add a sourcefolder;
builder.addSourceFolder( new File( "src/main/java" ) );
builder.addSourceFolder( new File( "target/generated-sources/foobar" ) );

// Add a custom ClassLoader
builder.addClassLoader( myCustomClassLoader );

// Ant example : add the <classpath> element's contents
builder.addClassLoader( new AntClassLoader( getProject(), classpath ) );
```

在解析任何源文件之前，必须添加额外的 ClassLoaders。


