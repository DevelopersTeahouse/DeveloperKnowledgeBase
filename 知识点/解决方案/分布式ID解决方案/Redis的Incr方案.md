# Redis 的 Incr 方案

- Redis Incr 命令将 key 中储存的数字值加一。如果 key 不存在，那么 key 的值会先被初始化为 0，然后再执行 INCR 操作，也就是第一个获取的数是 1，这样操作，可以每次都从 Redis 中获取唯一的 ID
- Java 代码实现

```java
Jedis jedis = new Jedis("127.0.0.1",6379);

try {

    long id = jedis.incr("id");

    System.out.println("从redis中获取的分布式id为：" + id);

} finally {

    if (null != jedis) {

        jedis.close();

    }

}
```
