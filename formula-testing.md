## STRING

Go to Administration > Entity Manager > any entity (which has a Description field) > Formula and paste the following formula:

<details>
    <summary><b>String</b> formula.</summary>

    description = list(
        string\concatenate('ab', 'cd'),                                     // will return 'abcd'
        string\substring('abcde', 1, 2),                                    // will return 'bc'
        string\substring('abcde', 1, -1),                                   // will return 'bcd'
        string\contains('hello world', 'world'),                            // will return true
        string\pos('hello world', 'world'),                                 // will return `6`
        string\test('hello world', '/hello/i'),                             // will return TRUE
        string\length('hello world'),                                       // will return `11`
        string\trim(' hello world '),                                       // will return `hello world`
        string\lowerCase('HELLO world'),                                    // will return `hello world`
        string\upperCase('HELLO world'),                                    // will return `HELLO WORLD`
        string\pad('100', 5, '*', 'right'),                                 // will return `100**`
        string\match('{token1} foo {token2} bar', '/{[^}]*}/'),             // will return {token1}
        string\matchAll('{token1} foo {token2} bar', '/{[^}]*}/'),          // will return {token1},{token2}
        string\matchExtract('values: 1000 2000', '/values\: (.*) (.*)$/'),  // will return 1000,2000
        string\replace('Hello {test}', '{test}', 'world'),                  // will return 'Hello world'
        string\split('hello world', ' ')                                    // will return ['hello', 'world']
        );

</details>
    
Then test the output of the formula in any record of the same entity.

<details>
<summary>Output example.</summary>
   
    abcd,bc,bcd,true,6,true,11,hello world,hello world,HELLO WORLD,100**,{token1},{token1},{token2},1000,2000,Hello world,hello,world
    
</details>

- [ ] **My string formula output is the same as in example.**

## DATETIME

Go to Administration > Entity Manager > any entity (which has a Description field) > Formula and paste the following formula:

<details>
    <summary><b>Datetime</b> formula:</summary>

    $datetime = '2023-03-21 13:15:19';
    $datetime1 = '2021-12-31 09:32:01';

    description = string\concatenate(
        datetime\today(),                                                    '\n', // will return today's date (w/o time)
        datetime\now(),                                                      '\n', // will return current datetime
        '\n',
        datetime\format($datetime, 'America/New_York', 'MM/DD/YYYY hh:mma'), '\n', // will return '03/21/2023 09:15am'
        datetime\date($datetime),                                            '\n', // will return 21
        datetime\month($datetime),                                           '\n', // will return 3
        datetime\year($datetime),                                            '\n', // will return 2023
        datetime\hour($datetime),                                            '\n', // will return 15
        datetime\minute($datetime),                                          '\n', // will return 15
        datetime\dayOfWeek($datetime),                                       '\n', // will return 2
        datetime\diff($datetime, $datetime1, 'years'),                       '\n', // will return 1
        datetime\diff($datetime, $datetime1, 'months'),                      '\n', // will return 14
        datetime\diff($datetime, $datetime1, 'days'),                        '\n', // will return 445
        datetime\diff($datetime, $datetime1, 'hours'),                       '\n', // will return 10683
        datetime\diff($datetime, $datetime1, 'minutes'),                     '\n', // will return 641023
        datetime\addMinutes($datetime, 10),                                  '\n', // will return 2023-03-21 13:25:19
        datetime\addMinutes($datetime, -10),                                 '\n', // will return 2023-03-21 13:05:19
        datetime\addHours($datetime, 7),                                     '\n', // will return 2023-03-21 20:15:19
        datetime\addHours($datetime, -7),                                    '\n', // will return 2023-03-21 06:15:19
        datetime\addDays($datetime, 14),                                     '\n', // will return 2023-04-04 13:15:19
        datetime\addDays($datetime, -14),                                    '\n', // will return 2023-03-07 13:15:19
        datetime\addWeeks($datetime, 4),                                     '\n', // will return 2023-04-18 13:15:19
        datetime\addWeeks($datetime, -4),                                    '\n', // will return 2023-02-21 13:15:19
        datetime\addMonths($datetime, 5),                                    '\n', // will return 2023-08-21 13:15:19
        datetime\addMonths($datetime, -5),                                   '\n', // will return 2022-10-21 13:15:19
        datetime\addYears($datetime, 10),                                    '\n', // will return 2033-03-21 13:15:19
        datetime\addYears($datetime, -10),                                   '\n', // will return 2013-03-21 13:15:19
        datetime\closest($datetime, 'date', 1, true),                        '\n', // will return 2023-02-28 22:00
        datetime\closest($datetime, 'time', '20:00'),                        '\n', // will return 2023-03-21 18:00
        datetime\closest($datetime, 'dayOfWeek', 1)                                // will return 2023-03-26 21:00
        );
    
</details>

Then test the output of the formula in any record of the same entity.

<details>
<summary>Output example:</summary>
   
    2023-04-04
    2023-04-04 13:40:47

    03/21/2023 09:15am
    21
    3
    2023
    15
    15
    2
    1
    14
    445
    10683
    641023
    2023-03-21 13:25:19
    2023-03-21 13:05:19
    2023-03-21 20:15:19
    2023-03-21 06:15:19
    2023-04-04 13:15:19
    2023-03-07 13:15:19
    2023-04-18 13:15:19
    2023-02-21 13:15:19
    2023-08-21 13:15:19
    2022-10-21 13:15:19
    2033-03-21 13:15:19
    2013-03-21 13:15:19
    2023-02-28 22:00
    2023-03-21 18:00
    2023-03-26 21:00
    
</details>

- [ ] **My datetime formula output is the same as in example.** *(Not counting the first two formulas that deal with today's date).*
