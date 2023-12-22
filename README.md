# Notities

How to

## Install

## How to use

### .gitattributes

/encrypted/* filter=crypt diff=crypt merge=crypt
$nameOfFile filter=crypt diff=crypt merge=crypt

# How to use:
# The base format of a new line is
# ' $nameOfFile filter=crypt diff=crypt merge=crypt '
# Copy this line to the top.
# Then uncomment it by removing the '#' 
# And change $nameOfFile to the name of your file 
# Or use the format '/$nameOfFolder/$nameOfFile' for a file in a subfolder
# Or use the format '/$nameOfFolder/*' for all files in a subfolder
# Standard format is with a subfolder called 'encrypted'
#
# Alternatively use the following commands :
# NOTE: replace '$sensitive_file' with the name of your file
#
# $ cd <path-to-your-repo>/ 
# $ echo '$sensitive_file filter=crypt diff=crypt merge=crypt' >> .gitattributes 
# $ git add .gitattributes $sensitive_file
# $ git commit -m 'Add encryped version of a sensitive file'
#
# This file should be committed and tracked along with everything else.
# This way clones will be aware of what is encrypted. Also it makes sure you don't accidentaly push an unencrypted file.
#
# MAKE SURE YOU DON'T ACCIDENTALY ENCRYPT THIS FILE! 

## Edge cases

## Good to know

## Standards

All instructions regarding permanent files like .gitattributes will also be in the file itself.


