# SHIYAN5
##实验目的

1.掌握字符串String及其方法的使用。

2.掌握文件的读取/写入方法。

3.掌握异常处理结构。

##实验内容
在某课上,学生要提交实验结果，该结果存储在一个文本文件A中。
文件A包括两部分内容：
一是学生的基本信息；

二是学生处理后的作业信息，该作业的业务逻辑内容是：利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能方法，实现如下功能：

##实验要求

1.每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”。

2.允许提供输入参数，统计古诗中某个字或词出现的次数。

3.输入的文本来源于文本文件B读取，把处理好的结果写入到文本文件A。

4.考虑操作中可能出现的异常，在程序中设计异常处理程序。

##实验步骤

1.采用Scanner类实例化学生:输入学生姓名，性别，年龄，编号。

2.创建文件的字节输入和输出流。

3.建立缓冲，增强文件读写能力。

4.用Handle处理字符。

5.最后使用write方法将学生基本信息写入目的文件。

##核心代码

 System.out.println("请输入要查询的字符：");
        String z = input.next();
        w = xms.getCharMaps(z,str1);

        System.out.println("******************学生信息*********************");
        Student dd = new Student();
        dd.setName("唐映枫");
        dd.setAge(21);
        dd.setNumber(2018310888);
        dd.setSex("男");
        System.out.println("学生姓名:" + dd.getName());
        System.out.println("学生年龄:" + dd.getAge());
        System.out.println("学生编号:" + dd.getNumber());
        System.out.println("学生性别:" + dd.getSex());

        System.out.println("处理完成");
        System.out.println(z + "出现次数为："+ z + "次");
    }
}
采用Scanner类实例化学生:输入学生姓名，性别，年龄，编号。

class Handle{
    public static StringBuffer Read(){
        String str1 = "";
        StringBuffer str2 = new StringBuffer(str1);
        try {
            File file = new File("C:\\Java\\File\\B.txt");
            FileReader fr = new FileReader(file);
            BufferedReader bReader = new BufferedReader(fr);
            while ((str1 =bReader.readLine()) != null) {
                str2.append(str1);
            }
            fr.close();


        } catch (IOException e) {
            e.printStackTrace();
        }
        return  str2;
    }
读取处理文本，整理文本输出。
##实验结果

请输入要查询的字符：
3
******************学生信息*********************
学生姓名:唐映枫
学生年龄:21
学生编号:2018310888
学生性别:男
作业处理完成
2出现的次数为：2次

##实验感想
通过这次实验，让我理解了字符串的含义，懂得了异常的处理方法，明白了缓冲流的作用，懂得了如何检验程序是否成功运行。
