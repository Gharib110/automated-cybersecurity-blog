---
title: "Sttr - Cross-Platform Cli App To Perform Various Operations On String"
date: Sat, 8 Jun 2024 08:30:00 -0400
draft: false
type: posts
categories: 
- Cli Tool,Devutils,Encrypt,Encryption Decryption,Sttr,Termux,Termux Tool,Tui App,Zeropad
---
# Sttr - Cross-Platform Cli App To Perform Various Operations On String

<br/>

<br/>
[![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgztwl3JFbuVcMwSU-_xvGbPGLexUNffx5nQ-x5o1ATps8Gjmp_pARhberO0vmkt4Tu7JTu-UTQdJiSmS4HTmq2sL3p3Kvn8UCWACaMHXoXpQtGuWzFu1epoqz-eiHkpfHOL24OPJbGdAjAfhXTGtMojMn1Nsc_KobRLVzjEbhPTnZpU2l_wDZ1Qez3VWrt/w640-h144/banner.png)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgztwl3JFbuVcMwSU-_xvGbPGLexUNffx5nQ-x5o1ATps8Gjmp_pARhberO0vmkt4Tu7JTu-UTQdJiSmS4HTmq2sL3p3Kvn8UCWACaMHXoXpQtGuWzFu1epoqz-eiHkpfHOL24OPJbGdAjAfhXTGtMojMn1Nsc_KobRLVzjEbhPTnZpU2l_wDZ1Qez3VWrt/s2720/banner.png)

  

`sttr` is command line software that allows you to quickly run various transformation [operations](https://www.kitploit.com/search/label/Operations "operations") on the string.

  

```
// With input promptsttr// Direct inputsttr md5 "Hello World"// File inputsttr md5 file.textsttr base64-encode image.jpg// Reading from different processor like cat, curl, printf etc..echo "Hello World" | sttr md5cat file.txt | sttr md5// Writing output to a filesttr yaml-json file.yaml > file-output.json
```

:movie\_camera: Demo
====================

[![](https://blogger.googleusercontent.com/img/a/AVvXsEifZ7QDJdSNZEXFfz05NMdeveSmLfqC6HcjM_9gGjbtt7gCXpJ5WgEQOjHA6nj1niO0PNhikPJ7ijaI3-_RsgF8dniUqwoxhatW7cYPV4oDEkzfBPngHXDFnT_mW4EA8_rTu2Cu6yABYEmRWg7HAiW1Xh6JEbzYp_S8b2ot4lkXTFCRkJAgeOVQDHzzaU4=w640-h436)](https://blogger.googleusercontent.com/img/a/AVvXsEifZ7QDJdSNZEXFfz05NMdeveSmLfqC6HcjM_9gGjbtt7gCXpJ5WgEQOjHA6nj1niO0PNhikPJ7ijaI3-_RsgF8dniUqwoxhatW7cYPV4oDEkzfBPngHXDFnT_mW4EA8_rTu2Cu6yABYEmRWg7HAiW1Xh6JEbzYp_S8b2ot4lkXTFCRkJAgeOVQDHzzaU4)

:battery: Installation
======================

#### Quick install

You can run the below `curl` to install it somewhere in your PATH for easy use. Ideally it will be installed at `./bin` folder

```
curl -sfL https://raw.githubusercontent.com/abhimanyu003/sttr/main/install.sh | sh
```

#### Webi

**[MacOS](https://www.kitploit.com/search/label/MacOS "MacOS") / [Linux](https://www.kitploit.com/search/label/Linux "Linux")**

```
curl -sS https://webi.sh/sttr | sh
```

**[Windows](https://www.kitploit.com/search/label/Windows "Windows")**

```
curl.exe https://webi.ms/sttr | powershell
```

See [here](https://webinstall.dev/sttr/ "here")

#### Homebrew

If you are on macOS and using Homebrew, you can install `sttr` with the following:

```
brew tap abhimanyu003/sttrbrew install sttr
```

#### Snap

```
sudo snap install sttr
```

#### Arch Linux

```
yay -S sttr-bin
```

#### Scoop

```
scoop bucket add sttr https://github.com/abhimanyu003/scoop-bucket.gitscoop install sttr
```

#### Go

```
go install github.com/abhimanyu003/sttr@latest
```

#### Manually

Download the pre-compiled binaries from the [Release!](https://github.com/abhimanyu003/sttr/releases "Release!") page and copy them to the desired location.

:books: Guide
=============

-   After installation simply run `sttr` command.

```
// For interactive menusttr// Provide your input// Press two enter to open operation menu// Press `/` to filter various operations.// Can also press UP-Down arrows select various operations.
```

-   Working with help.

```
sttr -h// Examplesttr zeropad -hsttr md5 -h
```

-   Working with files input.

```
sttr {command-name} {filename}sttr base64-encode image.jpgsttr md5 file.txtsttr md-html Readme.md
```

-   Writing output to file.

```
sttr yaml-json file.yaml > file-output.json
```

-   Taking input from other command.

```
curl https: //jsonplaceholder.typicode.com/users | sttr json-yaml
```

-   Chaining the different processor.

```
sttr md5 hello | sttr base64-encodeecho "Hello World" | sttr base64-encode | sttr md5
```

:boom: Supported Operations
===========================

#### Encode/Decode

-   \[x\] **ascii85-encode** - Encode your text to ascii85
-   \[x\] **ascii85-decode** - Decode your ascii85 text
-   \[x\] **base32-decode** - Decode your base32 text
-   \[x\] **base32-encode** - Encode your text to base32
-   \[x\] **base64-decode** - Decode your base64 text
-   \[x\] **base64-encode** - Encode your text to base64
-   \[x\] **base85-encode** - Encode your text to base85
-   \[x\] **base85-decode** - Decode your base85 text
-   \[x\] **base64url-decode** - Decode your base64 url
-   \[x\] **base64url-encode** - Encode your text to url
-   \[x\] **html-decode** - Unescape your HTML
-   \[x\] **html-encode** - Escape your HTML
-   \[x\] **rot13-encode** - Encode your text to ROT13
-   \[x\] **url-decode** - Decode URL entities
-   \[x\] **url-encode** - Encode URL entities

#### Hash

-   \[x\] **bcrypt** - Get the Bcrypt hash of your text
-   \[x\] **md5** - Get the MD5 checksum of your text
-   \[x\] **sha1** - Get the SHA1 checksum of your text
-   \[x\] **sha256** - Get the SHA256 checksum of your text
-   \[x\] **sha512** - Get the SHA512 checksum of your text

#### String

-   \[x\] **camel** - Transform your text to CamelCase
-   \[x\] **kebab** - Transform your text to kebab-case
-   \[x\] **lower** - Transform your text to lower case
-   \[x\] **reverse** - Reverse Text ( txeT esreveR )
-   \[x\] **slug** - Transform your text to slug-case
-   \[x\] **snake** - Transform your text to snake\_case
-   \[x\] **title** - Transform your text to Title Case
-   \[x\] **upper** - Transform your text to UPPER CASE

#### Lines

-   \[x\] **count-lines** - Count the number of lines in your text
-   \[x\] **reverse-lines** - Reverse lines
-   \[x\] **shuffle-lines** - Shuffle lines randomly
-   \[x\] **sort-lines** - Sort lines alphabetically
-   \[x\] **unique-lines** - Get unique lines from list

#### Spaces

-   \[x\] **remove-spaces** - Remove all spaces + new lines
-   \[x\] **remove-newlines** - Remove all new lines

#### Count

-   \[x\] **count-chars** - Find the length of your text (including spaces)
-   \[x\] **count-lines** - Count the number of lines in your text
-   \[x\] **count-words** - Count the number of words in your text

#### RGB/Hex

-   \[x\] **hex-rgb** - Convert a #hex-color code to RGB
-   \[x\] **hex-encode** - Encode your text Hex
-   \[x\] **hex-decode** - Convert Hexadecimal to String

#### JSON

-   \[x\] **json** - Format your text as JSON
-   \[x\] **json-escape** - JSON Escape
-   \[x\] **json-unescape** - JSON Unescape
-   \[x\] **json-yaml** - Convert JSON to YAML text
-   \[x\] **json-msgpack** - Convert JSON to MSGPACK
-   \[x\] **msgpack-json** - Convert MSGPACK to JSON

#### YAML

-   \[x\] **yaml-json** - Convert YAML to JSON text

#### Markdown

-   \[x\] **markdown-html** - Convert Markdown to HTML

#### Extract

-   \[x\] **extract-emails** - Extract emails from given text
-   \[x\] **extract-ip** - Extract IPv4 and IPv6 from your text
-   \[x\] **extract-urls** - Extract URls your text ( we don't do ping check )

#### Other

-   \[x\] **escape-quotes** - escape single and double quotes from your text
-   \[x\] **completion** - generate the autocompletion script for the specified shell
-   \[x\] **interactive** - Use sttr in interactive mode
-   \[x\] **version** - Print the version of sttr
-   \[x\] **zeropad** - Pad a number with zeros
-   \[x\] **and adding more....**

Featured On
===========

These are the few locations where `sttr` was highlighted, many thanks to all of you. Please feel free to add any blogs/videos you may have made that discuss `sttr` to the list.

-   [Youtube: The Giants of Open Source - DevOps Paradox](https://youtu.be/4nFRKbY_HVE?t=2529?ref=abhimanyu003/sttr "Youtube: The Giants of Open Source - DevOps Paradox")
-   [Terminal Trove - Tool of the Week](https://terminaltrove.com/sttr/?ref=abhimanyu003/sttr "Terminal Trove - Tool of the Week")
-   [nixCraft](https://www.cyberciti.biz/open-source/sttr-awesome-linux-unix-command-tool-for-transformation-string/?ref=abhimanyu003/sttr "nixCraft")

  
  

**[Download Sttr](https://github.com/abhimanyu003/sttr "Download Sttr")**

<br/>
[Source](http://www.kitploit.com/2024/06/sttr-cross-platform-cli-app-to-perform.html)
---
