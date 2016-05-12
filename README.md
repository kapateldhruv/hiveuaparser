# hiveuaparser
user agent parser for apache hive

## Credits
Derived from https://github.com/tobie/ua-parser/tree/master/java

## Compiling
This project uses Maven. Create your own jar by running

```
mvn package
```

## Usage

```
ADD JAR hiveuaparser-0.0.1-SNAPSHOT.jar;
CREATE TEMPORARY FUNCTION useragentparser AS 'kapatel.dhruv.hiveuaparser.HiveuaparserUDF';
SELECT useragentparser(agent,"USERAGENT_FAMILY") FROM table_name 
```
### FUNC(String useragentString, String attributeName)

###### attributeName
Allows you to extract specific property of useragent string.

+ USERAGENT_FAMILY
+ USERAGENT_MAJOR
+ USERAGENT_MINOR
+ OS_FAMILY
+ OS_MAJOR
+ OS_MINOR
+ DEVICE_FAMILY
