# Scoped

A simple dependency injection library built on Zones.

[![codecov](https://codecov.io/gh/rkishan516/scoped_zone/graph/badge.svg?token=XT56ZX5NL5)](https://codecov.io/gh/rkishan516/scoped_zone)

<a href="https://pub.dev/packages/scoped_zone" target="_blank">
    <img src="https://img.shields.io/pub/v/scoped_zone.svg?style=for-the-badge&label=pub&logo=dart"/> 
</a>
<a href="https://github.com/rkishan516/scoped_zone/tree/main/LICENSE" target="_blank">
  <img src="https://img.shields.io/github/license/rkishan516/scoped_zone.svg?style=for-the-badge&color=purple"/> 
</a>
<a href="https://github.com/rkishan516/scoped_zone/stargazers" target="_blank">
  <img src="https://img.shields.io/github/stars/rkishan516/scoped_zone.svg?style=for-the-badge&label=GitHub Stars&color=gold"/>
</a>
<br/>
<a href="https://pub.dev/packages/scoped_zone/score" target="_blank">
  <img src="https://img.shields.io/pub/likes/scoped_zone.svg?style=for-the-badge&color=1e7b34&label=likes&labelColor=black"/>
  <img src="https://img.shields.io/pub/points/scoped_zone?style=for-the-badge&color=0056b3&label=Points&labelColor=black"/>
  <img src="https://img.shields.io/pub/popularity/scoped_zone.svg?style=for-the-badge&color=c05600&label=Popularity&labelColor=black"/>
</a>

## Quick Start

```dart
import 'package:scoped_zone/scoped.dart';

final value = create(() => 42);

void main() {
  runScoped(scopeA, values: {value});
}

void scopeA() {
  print(read(value)); // 42
  runScoped(scopeB, values: {value.overrideWith(() => 0)});
}

void scopeB() {
  print(read(value)); // 0
}
```
