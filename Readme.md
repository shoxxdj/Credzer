# Credzer 

One to rule them all password manager.
Usefull to agregate datas from NTDS dump, hashcat results, responder captures .. 

## Setup 

``` poetry install ```

## Usage 

### Insert Datas

``` poetry run credzer -db <dblocation> --source ntlmv2 <file_containing_ntlmv2> ```
``` poetry run credzer -db <dblocation> --source hashcat_ntlmv2 <hashcat_potfile_after_ntlmv2_crack> ```

### Search content 

Print all cleartext passwords with domain\user:password syntax :
``` poetry run credzer -db <dblocation> --search cleartext ```
