# Record
编程记录

##所有文件都是以字节码的方式存储在硬盘上的 不同的字节码文件通过不同的解释器程序通过响应的字节码表编译

## 从文件往内存读 输入 InputStream /  从内存往硬盘写 输出 OutputStream 这两类都是IO读取的底层抽象类

基本读取

```java
   public static void FileRead() throws IOException{
       InputStreaam IS = new FileInputStream("文件路径");
       
       int readByte = 0;
       
       //读取完毕无字节时read方法返回 -1
       while((readByte = IS.read()) != -1) {
          System.out.print((char) readByte);
       }
       
   }
```

基本写入硬盘
```java
public static void FileWrite() {
     OutputStream OS = new FileOutputStream("文件路径");
     
     OS.write(字节);
}
```

File 文件类

```java
   File file = new File(文件路径);
   //判断实例指向地址是否是一个文件
   file.isFile() 
   //判断实例指向地址是否是一个文件夹
   file.isDirectory()
   //判断实例指向地址是否存在
   file.exists() 
   //获取实例指向地址的绝对路径
   file.getAbsolutePath()
   //获取实例指向地址下文件名
   file.lastFiles()
   //获取实例指向地址下文件名
   file.list()
   //判断当前实例指向地址是否是绝对路径
   file.isAbsolute()
   
   //拿到文件指定子目录
   File Home = new File(文件路径);
   File sub = new File(Home,文件目录名)
```


