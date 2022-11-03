# PHP Firebird Database Extension

You can find pre-compiled extension for `php 8.0.19` in `/src` folder

## How to compile - interbase.so
1. First clone the source repository to you local machine
```bash
https://github.com/FirebirdSQL/php-firebird.git
```
2. Cd into folder
```bash
cd php-firebird
```

3. Prepare the build environment for a PHP extension

```bash
phpize

CPPFLAGS=-I/Library/Frameworks/Firebird.framework/Versions/Current/Headers LDFLAGS=-L/Library/Frameworks/Firebird.framework/Versions/Current/Libraries ./configure
```

4. Compile

```bash
make
```

5. Finally, copy `interbase.so` in `php-firebird/module` into php extension folder and add

```ini
extension=interbase.so
```

## How to compile - pdo_firebird.so

1. First clone the source repository to you local machine

```bash
git clone https://github.com/php/php-src
```
| Note: be sure to checkout to tag which match your php version! |
| --- |

2. Cd into extension folder

```bash
cd php-src/ext/pdo_firebird
```

3. Prepare the build environment for a PHP extension

```bash
phpize

CPPFLAGS=-I/Library/Frameworks/Firebird.framework/Versions/Current/Headers LDFLAGS=-L/Library/Frameworks/Firebird.framework/Versions/Current/Libraries ./configure
```

4. Compile

```bash
make
```

5. Finally, copy `pdo_firebird.so` in `php-src/ext/pdo_firebird/module` into php extension folder and add

```ini
extension=pdo_firebird.so
```
