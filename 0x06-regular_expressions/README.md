# 0x06-regular_expressions

This directory contains several Ruby files that demonstrate the use of regular expressions.

## Files
1. **0-simply_match_school.rb**: This file demonstrates simple regular expressions to match certain patterns.
2. **1-repetition_token_0.rb**: This file showcases the usage of repetition tokens in regular expressions.
3. **100-textme.rb**: This file contains regular expressions to extract specific information from text messages.
4. **2-repetition_token_1.rb**: Similar to `1-repetition_token_0.rb`, this file explores more complex repetition tokens.
5. **3-repetition_token_2.rb**: This file continues the exploration of repetition tokens with different patterns.
6. **4-repetition_token_3.rb**: Another file demonstrating repetition tokens with varied patterns.
7. **5-beginning_and_end.rb**: This file illustrates the usage of anchors to match the beginning and end of lines.
8. **6-phone_number.rb**: Contains regular expressions to validate and extract phone numbers from text.
9. **7-OMG_WHY_ARE_YOU_SHOUTING.rb**: This file targets the identification of shouting text using regular expressions.

## The basics of regular expressions (cheat sheet)

| Character | What does it do?        | Example    | Matches                  |
|-----------|-------------------------|------------|--------------------------|
| ^         | Matches beginning of line | ^abc       | abc abcdef.., abc123     |
| $         | Matches end of line     | abc$       | my:abc, 123abc, theabc   |
| .         | Match any character     | a.c        | abc, asg, a2c            |
| \|        | OR operator             | abc\|xyz  | abc or xyz               |
| (...)     | Capture anything matched | (a)b(c)   | Captures 'a' and 'c'     |
| (?:...)   | Non-capturing group    | (a)b(?:c) | Captures 'a' but only groups 'c' |
| [...]     | Matches anything contained in brackets | [abc] | a,b, or c            |
| [^...]    | Matches anything not contained in brackets | [^abc] | xyz, 123, 1de       |
| [a-z]     | Matches any characters between 'a' and 'z' | [b-z] | bc, mind, xyz     |
| {x}       | The exact 'x' amount of times to match   | (abc){2} | abcabc           |
| {x,}      | Match 'x' amount of times or more       | (abc){2,} | abcabc, abcabcabc |
| {x,y}     | Match between 'x' and 'y' times.        | (a){2,4}  | aa, aaa, aaaaa   |
| *         | Greedy match that matches everything in place of the * | ab*c | abc, abbcc, abcdc |
| +         | Matches character before + one or more times | a+c | ac, aac, aaac       |
| ?         | Matches the character before the ? zero or one times. Also, used as a non-greedy match | ab?c | ac, abc |
| \         | Escape the character after the backslash or create an escape sequence. | a\sc | a c within the table |

## Usage

These files can be used to understand and practice regular expressions in Ruby.

## License

This directory and its contents are licensed to ALX Holberton School.
