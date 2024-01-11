is a character combination consisting of a backslash `\` followed by a letter or combination of digits. They specify actions within a line or string of text.

Some special characters that needs the use of escape sequence are: 
`\` = Backslash
`"` = Double Quotation
`%` = Percent 

Some examples are:
`\n` = Newline
`\t` = Horizontal Tab
`\a` = Alert
`\b` = Backspace
`\e` = escape Character
`\f` = Formfeed Page Break
`\r` = Carriage Return
`\v` = Vertical Tab

if you want to print `"meow"` 
```C
printf("meow"); //this will cause an error
printf("\"meow\""); //this will NOT cause an error
```

Alternatively, you can use  single quotes. 
```c
printf("'meow'");  //'start'
```

However, you cannot use double quote surrounded by single quote
```C
printf('"meow"');  //ERROR
```