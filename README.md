# PCRE_old_brackets_php_to_new
Regular Expression for change opening bracket of php files when &lt;? to &lt;?php, used in linux terminal command of [find]

//Regular Expression for change opening bracket of php files when &lt;? to &lt;?php, used in linux terminal command of [find]

//when <? and end of the string
find . -exec sed -i 's+<?$+<?php +g' {} \;

//and one more option when no end string but some symbols after <? for example <? and space
find TEST_CACHE.php -exec sed -i 's+<?[^a-z]+<?php +g' {} \;
