## GPT 接口服务

> 使用 java 编写的 gpt api 接口服务 
> <br>
> JDK 17, Spring Boot 3.0.0

## 使用方法

### docker 启动

1. postman 中输入地址，请求类型为 post `http://ip:9876/question` ，设置请求体信息如下；

   ```json
   {
       "model": "gpt-3.5-turbo",
       "messages": [{"role": "user", "content": "Say this is a test!"}],
       "temperature": 0.7
   }
   ```

2. 确保本地代理正常可用，打开 `Allow LAN` 开关，确保局域网内设备可以正常访问；

3. 更改 `docker/app/application-docker.yml` 中的 `spring.gpt.service.proxy-address` 为自己代理地址；

4. 更改 `docker/app/application-docker.yml` 中的 `spring.gpt.service.apikey` 为自己的 apikey ；

5. 进入 docker-compose,yml 所在文件夹，运行 `docker-compose up -d` 启动服务。

### 本地启动

先做 1.2 idea 打开项目，更改 1.3 中的配置项。启动 `主类` 即可。



postman 调用效果展示：

<img src="./img/img.png">