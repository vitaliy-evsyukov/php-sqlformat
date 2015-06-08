Using some libraries of phpmyadmin,
Make the SQL look better.

Format your SQL.

Beautify your sql but also can turn your formatted sql into html code.

How to:

1. Download the libraries from : http://code.google.com/p/php-sqlformat/downloads/list
> Put them in your WEB dirctory

2. edit your php file
<pre>
<link rel="stylesheet" type="text/css" href="sqlparserlib/sqlsyntax.css" /><br>
<br>
<?php<br>
define('PARSER_LIB_ROOT', "/home/admin/www/sqlparserlib/");<br>
require_once PARSER_LIB_ROOT.'sqlparser.lib.php';<br>
function SQLFormatPHP($sql){<br>
return PMA_SQP_formatHtml(PMA_SQP_parse($sql));<br>
}<br>
<br>
$sql = "SELECT * FROM (select * from dual)";<br>
echo SQLFormatPHP($sql);<br>
?><br>
</pre>
Notice: /home/admin/www/sqlparserlib/  you must set this to your right PATH

3. screenshot

[![](http://farm6.static.flickr.com/5170/5366693389_6f140df551.jpg)](http://www.flickr.com/photos/26825745@N06/5366693389/)

4. if problem, mail me : orczhou@gmail.com