# Compare two files

`diff file_1 file_2`

=> Shows the differences between file_1 and file_2.

# Unified diff format

`diff -u file_1 file_2`

=> Shows the differences in unified format.

   This format is easier to read and is commonly used for patches.

# Text comparison for binary files

`diff --text file_1 file_2` or `diff -a file_1 file_2`

=> Treats all files as text, even if they might be binary files.

To see character-level differences between binary files.

# Create a patch file

`diff -u file_1 file_2 > a.patch`

=> Saves the unified diff output into a patch file.

# Apply a patch

`patch file_1 < a.patch`

=> Applies the changes from a.patch to file_1.

   After applying the patch successfully, file_1 should match file_2.

