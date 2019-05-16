--身份证相同，姓名不同
select * from dbo.全市公职人员名单 a join 疑点人员信息 b on a.统一18位身份证号=b.身份证号码 
 join dbo.企业信息 c on b.内部序号=c.内部序号
 --join dbo.企业变更信息 d on c.内部序号=d.内部序号
 where 企业状态='已成立' and replace(a.姓名,' ','')<>replace(b.姓名,' ','')
 --有一人
 
 --身份证相同，姓名也相同
select * from dbo.全市公职人员名单 a join 疑点人员信息 b on a.统一18位身份证号=b.身份证号码 
 join dbo.企业信息 c on b.内部序号=c.内部序号
 --join dbo.企业变更信息 d on c.内部序号=d.内部序号
 where 企业状态='已成立' and replace(a.姓名,' ','')=replace(b.姓名,' ','')
 
 
 --状态改变
 --1
 --2