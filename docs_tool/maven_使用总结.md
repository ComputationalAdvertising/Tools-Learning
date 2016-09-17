## Maven-Idea使用

### 查看pom依赖jar包的依赖树

```
mvn dependency:tree -Dverbose
```


### Maven引入本地jar包

一些没有用maven管理的jar包，有时需要在项目中依赖。maven编译和打包时需要将其引入。方法如下：

在pom文件配置：

```
<dependency>
	<groupId>com.meituan.dataapp</groupId>
	<artifactId>nlp</artifactId>
	<version>2.1</version>
	<scope>system</scope>
	<systemPath>${project.basedir}/src/main/resources/lib/MTWordSeg.jar</systemPath>	
</dependency>
```

system不可改。同时还需要在package时引入：

```
<build>
<resources>
            <!-- 这种方式可以将JAR包引入，还不清楚原因，待研究 -->
            <resource>
                <targetPath>lib/</targetPath>
                <directory>lib/</directory>
                <includes>
                    <include>**/MTWordSeg.jar</include>
                </includes>
            </resource>
        </resources>
</build>
```

> 这种方式虽然可以将本地jar打包进去，但是仍然提示找不到class，无法解压。