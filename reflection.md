# Lab 5 Reflection

## 1. Which issues were the easiest to fix, and which were the hardest? Why?

The easiest issues were formatting mistakes, unused imports, and naming errors because they were simple to fix. The hardest issues were related to security and program behaviour. For example, I had to change how the program runs scene commands without breaking its existing features. I also fixed a bug where changing one device's settings affected other devices.

## 2. Did the static analysis tools report any false positives? If so, describe one example.

Some warnings needed to be checked before deciding whether they were actual problems. For example, Bandit warned about the use of `subprocess` and `bash`. This does not always mean the code is unsafe, but it needs to be checked. I made the code safer by checking the scene path and avoiding `shell=True`.

## 3. How would you integrate static analysis tools into your actual software development workflow?

I would use Pylint and Flake8 to check code quality and formatting, and Bandit to find possible security issues. I would run these tools while writing code and before committing changes. I would also add them to automated checks so that problems are found before code is merged.

## 4. What tangible improvements did you observe in the code quality, readability, or potential robustness after applying the fixes?

The code became cleaner and easier to read. Removing unused imports and fixing naming and formatting issues improved its quality. Giving each device its own settings fixed the bug where changing one device affected others. I also made scene commands safer by checking their paths and avoiding `shell=True`. These changes made the program easier to maintain and less likely to have certain errors.
