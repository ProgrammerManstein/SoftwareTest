# 部署

> 如无额外说明，所有软件采用稳定版中最新的版本

建议安装windows terminal 作为终端


- 原生
    - 后端
   1. 安装maven并添加到环境变量
       链接： https://dlcdn.apache.org/maven/maven-3/3.8.5/binaries/apache-maven-3.8.5-bin.zip
   2. 安装postgresql，密码写root
   2. 命令行运行
   
    ```bash
    cd backend
    mvn install
    mvn springboot:run
    ```
   
    注意，此步耗时极长，半小时都很有可能
   
   如无报错，后端部署应该完成了
   
   4. idea配置
   
       第一次打开目录时，idea可能会给项目配置一个错误的工件,需要重新重新设置
   
       - 使用idea打开backend目录
       - 右上角点击，如果有shop-api这个应该是对的
           ![image-20220526194809774](D:\Archieved\MakrdownCache\deployment\image-20220526194809774.png)
       - 运行栏写springboot:run
       - ![image-20220526194853648](D:\Archieved\MakrdownCache\deployment\image-20220526194853648.png)
   
    - 前端
        1. 安装nodejs
        2. 命令行运行
         ```bash
         cd frontend
         npm install
         npm run ng serve
   
    
   
- 使用docker

    此步在software-test目录下完成

1. 安装docker

    >  注意：docker的安装可能与wsl有连带关系
    
 2. 使用命令行打开并运行
    ```bash
    cd software-test-docker
    docker-compose up --build
    ```
    > 注意，此步骤需要下载镜像，请保持VPN连接或换源，终端需要设置代理或VPN打开全局模式

3. 部署完成后，运行在localhost:80, 注意，此时VPN须关闭或使用PAC模式
