# 前言

欢迎来到本项目的Gitee仓库！这是一个基于SpringBoot和Vue的周边游平台个人管理系统的毕业设计项目。以下将为您详细介绍本项目的相关内容，包括技术选型、核心代码以及如何获取免费源码等。

## 内容介绍

本项目旨在为用户提供一个便捷、高效的周边游平台个人管理系统。通过使用Java语言和Spring Boot框架，结合前端技术Vue、JS和CSS3，实现了一套功能完善、易于使用的系统。用户可以轻松管理个人旅游相关信息，包括行程规划、景点推荐、住宿安排等。

## 技术介绍

- 语言：Java
- 使用框架：Spring Boot
- 前端技术：JS、Vue、CSS3
- 开发工具：IDEA/Eclipse
- 数据库：MySQL 5.7/8.0
- 数据库管理工具：phpstudy/Navicat
- JDK版本：jdk1.8
- Maven：apache-maven 3.8.1-bin
- 前端环境：Node.Js 12\14\16

## 核心代码

以下是本项目中的一段核心代码，展示了如何使用Spring Boot和Vue实现用户登录功能：

```java
// UserController.java
@RestController
public class UserController {

    @Autowired
    private UserService userService;

    @PostMapping("/login")
    public ResponseEntity<String> login(@RequestBody User user) {
        String token = userService.login(user.getUsername(), user.getPassword());
        if (token != null) {
            return ResponseEntity.ok(token);
        } else {
            return ResponseEntity.status(HttpStatus.UNAUTHORIZED).body("用户名或密码错误");
        }
    }
}
```

```javascript
// login.vue
export default {
  data() {
    return {
      username: '',
      password: ''
    };
  },
  methods: {
    async login() {
      try {
        const response = await this.$http.post('/login', {
          username: this.username,
          password: this.password
        });
        localStorage.setItem('token', response.data);
        this.$router.push('/home');
      } catch (error) {
        alert('用户名或密码错误');
      }
    }
  }
};
```

## 免费源码获取

```
5000套系统成品在线演示视频，复制到流浪器： 
```
```
https://www.yuque.com/yuqueyonghux32e1j/kxdc9g/ad8oz3bamkxmay0e#Cxun
```
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

# 项目截图

![封面图片](https://img14.360buyimg.com/ddimg/jfs/t1/323952/29/4628/153501/689de021Fa8ed7200/21b48368a15127ed.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/313890/28/26401/39737/689de000F21636fb1/a83c14af85ef102f.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/312061/12/26250/102734/689de000F1142eb5c/a5db79039fdb4bff.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/324068/25/4499/40167/689de001F0ca5e0c1/6bbfe7911565d1a9.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/325275/35/4601/48777/689de002Fe290511c/0fe038168443c92d.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/306948/8/26181/32108/689de002F04668d0d/c66a579b5453c8ed.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/319499/15/24561/73633/689de003Fc52d6d1e/24148f12a5ff3c99.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/325936/34/4511/63814/689de003F3a793210/6eaab6cc6ee08a5b.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/328259/29/4577/35879/689de004F02e217a1/43faea1b9b8a0274.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/306823/33/26215/39516/689de004F48e6aeaa/65a8ad1a60362dc5.jpg)


## 万字文档
![文档介绍](https://img14.360buyimg.com/ddimg/jfs/t1/338393/1/3576/156947/68b1ad0cF74dc525c/ff9cd6c574295685.jpg)
