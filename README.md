# chronoscala

A port of [nscala_time](https://github.com/nscala-time/nscala-time) to JSR-310.

## Requirements

- Java 8
- Scala 2.10.x or 2.11.x

## Installation

```scala
libraryDependencies += "jp.ne.opt" %% "chronoscala" % "0.0.2"
```

## Usage

```scala
import jp.ne.opt.chronoscala.Imports._

ZonedDateTime.now + 2.months // returns java.time.ZonedDateTime = 2016-09-12T02:24:22.724+09:00[Asia/Tokyo]

ZonedDateTime.now < ZonedDateTime.now + 1.month // returns true

ZonedDateTime.now to (ZonedDateTime.now + 1.day) // returns Interval(2016-07-11T19:15:42.641Z,2016-07-12T19:15:42.641Z)

(ZonedDateTime.now to (ZonedDateTime.now + 1.second)).millis // returns 1000

2.hours + 45.minutes + 10.seconds // returns PT2H45M10S

(2.hours + 45.minutes + 10.seconds).millis // returns 9910000

2.months + 3.days // returns P2M3D
```