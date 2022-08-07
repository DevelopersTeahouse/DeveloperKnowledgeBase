# UUID

- UUID 是字 Universally Unique Identifier，翻译为中文是 通用唯一标识符
- 产生重复的 UUID 并造成错误的概率非常低，一般可以不用考虑这个问题
- 在 Java 中要获取一个 UUID，可以使用 java.util 包提供的方法

```java
public class MyTest {

    public static void main(String[] args) {

        System.out.println(java.util.UUID.randomUUID().toString());

    }

}
```

## 缺点

- uuid 字符串特别的长，占用空间大
- uuid 生成的 id 很随机，索引效率也很低，想通过 uuid 做排序也基本不可能
