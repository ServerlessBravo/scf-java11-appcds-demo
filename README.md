# 通过 Web 函数 Spring Boot 应用

## 本地编译

    rm -rf build
    gradle build

    # 导出类的列表
    gradle generateClassList
    # 生成共享文件
    gradle generateAppCDSArchive
    # 本地以共享JSA文件的方式启动
    gradle RunApplicationWithAppCDS

## 本地打包

    gradle buildZip

    #查看部署目标
    tree build/distributions

    build/distributions
    └── tencent_scf-0.0.1-SNAPSHOT.zip

0 directories, 1 file

## 部署到 SCF

![Deploy](https://user-images.githubusercontent.com/251222/157162205-d5f4b120-1ddf-4fce-a852-2bb094ff4575.jpg)

修改函数配置：

![Configure](https://user-images.githubusercontent.com/251222/157162229-9605d95d-f975-4590-b7a5-fba0da93aa2f.jpg)

## 测试

![Test](https://user-images.githubusercontent.com/251222/157162214-7632437e-0e90-40d4-b7f0-3708c0818e54.jpg)

## 查看启动日志

![Check](https://user-images.githubusercontent.com/251222/157162241-1dc1de34-ed98-438b-9138-0f45bddf138e.jpg)

## Reference

- [Java 11 AppCDS example with Gradle](https://blog.jdbevan.com/2020/09/30/java-11-appcds-example-with-gradle/)
- [深度好文：云函数 SCF + KonaJDK11 + Spring + 提速降存一把梭](https://segmentfault.com/a/1190000039714331)
