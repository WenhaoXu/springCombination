# 这是一个对于spring 组合其他框架的demo练习
 
### 1.组合Ubuntu中docker的mysql 。
 1.1  映射Ubuntu的ip地址。
 1.2 为远程连接创建角色和权限；
      # docker 中下载 mysql
      docker pull mysql
      
      #启动
      docker run --name mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=Lzslov123! -d mysql
      
      #进入容器
      docker exec -it mysql bash
      
      #登录mysql
      mysql -u root -p
      ALTER USER 'root'@'localhost' IDENTIFIED BY 'Lzslov123!';
      
      #添加远程登录用户
      CREATE USER 'liaozesong'@'%' IDENTIFIED WITH mysql_native_password BY 'Lzslov123!';
      GRANT ALL PRIVILEGES ON *.* TO 'liaozesong'@'%';
### 2.组合jms 