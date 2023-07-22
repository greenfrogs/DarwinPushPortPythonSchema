# Darwin Push Port XML Schemas for Python
Darwin push port XML schema for Python v16 using generateDS

- generateDS: https://www.davekuhlman.org/generateDS.html
- Schema Source: https://wiki.openraildata.com/index.php?title=Darwin:Push_Port_XML_Schemas

## Setup
To generate updated files install [generateDS](https://sourceforge.net/projects/generateds/), add the schema files to `./schema` and run the following:

```
Single File:
$ python .\generateDS.py -f --use-source-file-as-module-name --one-file-per-xsd --external-encoding=utf-8 --output-directory ./darwin/ FILE_NAME

Multi File (pwsh):
$ Get-ChildItem -File ./schema | Foreach { python .\generateDS.py -f --use-source-file-as-module-name --one-file-per-xsd --external-encoding=utf-8 --output-directory ./darwin/ $_.fullname}
 ```
