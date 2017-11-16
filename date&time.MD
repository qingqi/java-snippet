1. 日期和时间计算，方法一：

```java
static final long MILLISECONDS_IN_A_DAY = 24 * 60 * 60 * 1000;

// now, From the source code, the no-arg constructor invokes System.currentTimeMillis() to get 
// the milliseconds since January 1, 1970, 00:00:00 GMT (known as "epoch") and stores in a private variable fastTime.
// Take note that epoch is absolute and does not depends on local time zones.
Date date = new Date(); 
long time = date.getTime(); // Returns the number of milliseconds since January 1, 1970, 00:00:00 GMT
Date dawn = new Date(time - time % MILLISECONDS_IN_A_DAY); // dawn of today
```

2. 日期格式化：
```java
DateFormat sdf = new SimpleDateFormat("yyyyMMddHHmm");
sdf.setTimeZone(TimeZone.getTimeZone("GMT")); // 注意设置时区，默认是系统的时区
Date = sdf.parse("201708051200");
```
y 年，M 月，d 日，h 时，在上午或下午，H 时，在一天中，m 分，s 秒，S 毫秒，E 星期


3. Calendar
Calendar = Date(time since epoch) + timezone + locale
