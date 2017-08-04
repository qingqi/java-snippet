日期和时间计算，方法一：

```java
static final long MILLISECONDS_IN_A_DAY = 24 * 60 * 60 * 1000;

Date date = new Date(); // now
long time = date.getTime(); // Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT
Date dawn = new Date(time - time % MILLISECONDS_IN_A_DAY); // dawn of today
```
