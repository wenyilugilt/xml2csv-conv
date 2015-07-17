xml2csv-conv is command line tool for converting data from XML schema to CSV. The tool has many command line options. The software is platform independent and was written in Java language.


## Features ##
  * Converts XML schema to CSV file
  * Can deal with filenames and urls
  * Automatically detects loops (repeated elements) in XML used for splitting data to rows
  * Allows to override name of the loop/repeated field
  * Allows to keep only specific tags/fields
  * Allows to ignore specific tags/fields
  * Allows to set values for empty data and CSV separator
  * Supports distinct option
  * Platform Independent


## Usage ##
**Syntax**
<pre>
java -jar xml2csv-conv.jar [-options] <source filename or url> <destination filename><br>
xml2csv-conv [-options] <source filename or url> <destination filename><br>
</pre>

**Options**
<pre>
-l <field name>                 Allows to set the name of the field that<br>
repeats in XML schema.<br>
-k <list of fields' names>      Field' names that will be kept,<br>
separated by comma without space.<br>
-i <list of fields' names>      Field' names that will be ignored,<br>
separated by comma without space.<br>
-d                              Returns not duplicated rows.<br>
-e <value>                      Value for empty data, e.g. "-"<br>
-s <value>                      Value for separator in CSV, e.g. ","<br>
</pre>

**Usage examples**
<pre>
xml2csv-conv -l field -i city,country -d -s "," data.xml data.csv<br>
xml2csv-conv -k "name, surname" data.xml data.csv<br>
xml2csv-conv http://www.example.com/data.xml data.csv<br>
xml2csv-conv data.xml data.csv<br>
</pre>


## Screenshots ##
![http://xml2csv-conv.googlecode.com/svn/trunk/misc/screenshot.png](http://xml2csv-conv.googlecode.com/svn/trunk/misc/screenshot.png)

## Credits ##
Thanks to Donetsk National Technical University  (http://en.wikipedia.org/wiki/Donetsk_National_Technical_University) and Victor Babkov (http://osum.sun.com/profile/VictorSBabkov) who taught me JAVA.