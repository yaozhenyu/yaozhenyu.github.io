# Pl/Sql

```
PL/SQL块的结构如下：

DECLARE 
/* 声明部分: 在此声明PL/SQL用到的变量,类型及游标，以及局部的存储过程和函数 */
BEGIN
    /*  执行部分:  过程及SQL 语句  , 即程序的主要部分  */
EXCEPTION
   /* 执行异常部分: 错误处理  */
END;
```

```
DECLARE
v_num NUMBER ; -- 定义一个变量v_num
BEGIN
v_num := 30 ; -- 设置v_num的内容
DBMS_OUTPUT.put_line('V_NUM变量的内容是：' || v_num) ;
END ;
/
```

**function**

```
create or replace function fun_info(i_eno number,o_title out varchar2,salch in out number) return varchar2
as
name emp.ename%type;
begin
select ename into name from emp where empno=i_eno;
update emp set sal=sal+salch where empno=i_eno returning job,sal into o_title,salch;
return name;
end;

// 删除function
drop function fun_info;
```

**procedure**

```
---创建procedure   
　　create or replace procedure up_sel(cur_test out sys_refcursor)   
　　is   
　　begin   
　　open cur_test for   
　　select * from a;   
　　end;

　　--删除存储过程   
　　drop procedure up_sel   
　　--提交   
　　commit   
　　----在PL/sql中执行procedure------   
　　---//   file-->>new -->>test window   
　　begin   
　　-- Call the procedure   
　　up_sel(cur_test => :cur_test);   
　　end;   
　　--//在variable中填入定义的游标名  cur_test   
　　--//在Type中填入游标类型  Cursor   
　　--//点击Value 右边的 ...图标即可显示出所要的结果
```

**赋值用 :=**

`various := 1;`

