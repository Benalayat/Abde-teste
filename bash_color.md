In Bash, you can add colors to strings printed in the terminal using ANSI escape codes. ANSI escape codes are special sequences of characters that control various text formatting, including colors. Here's how you can use them to add colors to your strings:

1. **Foreground Colors**:
   - `\e[30m`: Black
   - `\e[31m`: Red
   - `\e[32m`: Green
   - `\e[33m`: Yellow
   - `\e[34m`: Blue
   - `\e[35m`: Magenta
   - `\e[36m`: Cyan
   - `\e[37m`: White

2. **Background Colors**:
   - `\e[40m`: Black
   - `\e[41m`: Red
   - `\e[42m`: Green
   - `\e[43m`: Yellow
   - `\e[44m`: Blue
   - `\e[45m`: Magenta
   - `\e[46m`: Cyan
   - `\e[47m`: White

3. **Text Formatting**:
   - `\e[0m`: Reset all formatting (including color) to default.
   - `\e[1m`: Bold
   - `\e[2m`: Dim
   - `\e[4m`: Underline
   - `\e[5m`: Blink
   - `\e[7m`: Invert colors (swap foreground and background)

Here's an example of how to use these escape codes in a Bash script:

```bash
#!/bin/bash

# Print a red "Hello" with a green background and bold text.
echo -e "\e[31;42;1mHello\e[0m"

# Reset formatting and print a yellow "World" with a blue background.
echo -e "\e[0m\e[33;44mWorld\e[0m"
```

In the above example, `-e` is used with `echo` to enable the interpretation of escape codes.

You can customize the colors and formatting according to your needs by combining the appropriate escape codes. Just remember to use `\e[0m` to reset the formatting at the end of the colored text to avoid affecting the rest of your terminal output.