# Java8新日期API

## now方法1

基本使用

```java
// 时间线上的一个瞬间点。
// 此类模拟时间线上的单个瞬时点。这可用于在应用程序中记录事件时间戳。
Instant instantNow = Instant.now();
// 日历系统中没有时区的日期，可用于存储生日
LocalDate localDateNow = LocalDate.now();
// 日历系统中没有时区的时间
LocalTime localTimeNow = LocalTime.now();
// 日历系统中没有时区的日期时间
LocalDateTime localDateTimeNow = LocalDateTime.now();
// 日历系统中具有时区的日期时间
ZonedDateTime zonedDateTimeNow = ZonedDateTime.now();

System.out.println("instantNow = " + instantNow);
System.out.println("localDateNow = " + localDateNow);
System.out.println("localTimeNow = " + localTimeNow);
System.out.println("localDateTimeNow = " + localDateTimeNow);
System.out.println("zonedDateTimeNow = " + zonedDateTimeNow);
```

输出结果

```java
instantNow = 2022-03-20T01:35:32.074Z
localDateNow = 2022-03-20
localTimeNow = 09:35:32.115
localDateTimeNow = 2022-03-20T09:35:32.115
zonedDateTimeNow = 2022-03-20T09:35:32.115+08:00[Asia/Shanghai]
```

## now方法2

基本使用

```java
// 日历系统中的年
Year year = Year.now();
// 日历系统中的年月
YearMonth yearMonth = YearMonth.now();
// 日历系统中的月日
MonthDay monthDay = MonthDay.now();
System.out.println("year = " + year);
System.out.println("yearMonth = " + yearMonth);
System.out.println("monthDay = " + monthDay);
```

输出结果

```java
year = 2022
yearMonth = 2022-03
monthDay = --03-20
```

