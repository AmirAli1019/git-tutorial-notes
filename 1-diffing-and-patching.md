# Compare two files

`diff file_1 file_2`

=> Shows the differences between file_1 and file_2.

# Unified diff format

`diff -u file_1 file_2`

=> Shows the differences in unified format.

   This format is easier to read and is commonly used for patches.

# Create a patch file

`diff -u file_1 file_2 > a.patch`

=> Saves the unified diff output into a patch file.

# Apply a patch

`patch file_1 < a.patch`

=> Applies the changes from a.patch to file_1.

   After applying the patch successfully,

   file_1 should match file_2.
