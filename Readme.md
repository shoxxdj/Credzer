# Credzer 

One to rule them all password manager.
Usefull to agregate datas from NTDS dump, hashcat results, responder captures .. 

## Setup 

``
poetry install
```
or
```
pip install credzer
```



## Usage 

### Help 

```
usage: credzer [-h] --database DATABASE [--source {cme,msf,donpapi,ntds,hashcat_ntlm,ntlmv2,hashcat_ntlmv2}] [--file FILE] [--search SEARCH]

    Credzer - $$$
    Version : 0.1 Codename : One to rule them all
    

options:
  -h, --help            show this help message and exit
  --database DATABASE, -db DATABASE
                        the final db
  --source {cme,msf,donpapi,ntds,hashcat_ntlm,ntlmv2,hashcat_ntlmv2}, -s {cme,msf,donpapi,ntds,hashcat_ntlm,ntlmv2,hashcat_ntlmv2}
  --file FILE, -f FILE  File containing creds to be add to the database
  --search SEARCH       Search content in the database

```


### Insert Datas

``` 
poetry run credzer -db <dblocation> --source ntlmv2 <file_containing_ntlmv2> 
poetry run credzer -db <dblocation> --source hashcat_ntlmv2 <hashcat_potfile_after_ntlmv2_crack> 
```

### Search content 

Print all cleartext passwords with domain\user:password syntax :
``` 
poetry run credzer -db <dblocation> --search cleartext 
```

## Todolist

- [ ] Add support for CMEDB
- [ ] Add support for MSFDB
- [ ] Add support for Donpapi files
- [ ] Improve search content and syntax
- [ ] Better pretty print
