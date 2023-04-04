```
description = list(
    string\concatenate('ab', 'cd'), 
    string\substring('abcde', 1, 2),
    string\substring('abcde', 1, -1),
    string\contains('hello world', 'world'),
    string\pos('hello world', 'world'),
    string\test('hello world', '/hello/i'), 
    string\length('hello world'),
    string\trim(' hello world '),
    string\lowerCase('HELLO world'),
    string\upperCase('HELLO world'),
    string\pad('100', 5, '*', 'right'),
    string\match('{token1} foo {token2} bar', '/{[^}]*}/'),
    string\matchAll('{token1} foo {token2} bar', '/{[^}]*}/'),
    string\matchExtract('values: 1000 2000', '/values\: (.*) (.*)$/'),
    string\replace('Hello {test}', '{test}', 'world'),
    string\split('hello world', ' ')
    );
```

Output in description: 

```
abcd,bc,bcd,true,6,true,11,hello world,hello world,HELLO WORLD,100**,{token1},{token1},{token2},1000,2000,Hello world,hello,world
```
