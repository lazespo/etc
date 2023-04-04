## STRING

Go to Administration > Entity Manager > any entity (which has a Description field) > Formula and paste the following formula:

```
description = list(
    string\concatenate('ab', 'cd'); // will return 'abcd'
    string\substring('abcde', 1, 2); // will return 'bc'
    string\substring('abcde', 1, -1); // will return 'bcd'
    string\contains('hello world', 'world') // will return true
    string\pos('hello world', 'world') // will return `6`
    string\test('hello world', '/hello/i') // will return TRUE
    string\length('hello world') // will return `11`
    string\trim(' hello world ') // will return `hello world`
    string\lowerCase('HELLO world') // will return `hello world`
    string\upperCase('HELLO world') // will return `HELLO WORLD`
    string\pad('100', 5, '*', 'right') // will return `100**`
    string\match('{token1} foo {token2} bar', '/{[^}]*}/') // will return {token1}
    string\matchAll('{token1} foo {token2} bar', '/{[^}]*}/') // will return {token1},{token2}
    string\matchExtract('values: 1000 2000', '/values\: (.*) (.*)$/') // will return 1000,2000
    string\replace('Hello {test}', '{test}', 'world') // will return 'Hello world'
    string\split('hello world', ' ') // will return ['hello', 'world']
    );
```

Then test the output of the formula in any record of the same entity.

*Output in your description*:

```

```

<details>
<summary>Output example:</summary>
   
    abcd,bc,bcd,true,6,true,11,hello world,hello world,HELLO WORLD,100**,{token1},{token1},{token2},1000,2000,Hello world,hello,world
    
</details>
