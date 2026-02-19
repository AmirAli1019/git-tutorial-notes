diff file_1 file_2 ==> Shows the difference between two files
diff file_1 file_2 -u ==> Displays the difference between two files in a way that is easier to read for both humans and computers.
diff file_1 file_2 > a.patch ==> Saves the difference in a patch file.

patch file_1 < a.patch ==> Patches the older file based on the generated patch file, After patching file_1 and file_2 will be identical.
