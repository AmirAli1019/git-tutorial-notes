A .gitignore file tells Git which files and folders it should not track or include in a repository.

A sample gitignore:

```bash
# Ignore a specific file
secret.txt

# Ignore a specific directory
node_modules/

# Ignore by extension (all .log files)
*.log

# Ignore files starting with "temp"
temp*

# Match a single character (Matches file1.txt and file2.txt but not file10.txt)
file?.txt

# Ignore a specific path
build/output.txt

# Ignore a directory completely
build/

# Ignore any file OR directory named "cache" at any depth
**/cache

# Ignore only directories named "cache"
**/cache/

# Ignore all .log files except one
*.log
!important.log
```
