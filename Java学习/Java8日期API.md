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

## of方法

基本使用

```java
// 指定年月日
LocalDate localDate = LocalDate.of(2000, 7, 7);
// 指定时分秒
LocalTime localTime = LocalTime.of(12, 3, 6);
// LocalDateTime的特殊使用
LocalDateTime localDateTime1 = LocalDateTime.of(localDate, localTime);
LocalDateTime localDateTime2 = LocalDateTime.of(2000, 7, 7, 12, 3, 6);

System.out.println("localDate = " + localDate);
System.out.println("localTime = " + localTime);
System.out.println("localDateTime1 = " + localDateTime1);
System.out.println("localDateTime2 = " + localDateTime2);
```

输出结果

```java
localDate = 2000-07-07
localTime = 12:03:06
localDateTime1 = 2000-07-07T12:03:06
localDateTime2 = 2000-07-07T12:03:06
```

## 时区

```java
// 获取所有时区
Set<String> availableZoneIds = ZoneId.getAvailableZoneIds();
for (String availableZoneId : availableZoneIds) {
	System.out.println(availableZoneId);
}
// 获取当前系统时区
ZoneId zoneId = ZoneId.systemDefault();
System.out.println("zoneId = " + zoneId);
```

