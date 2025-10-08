## binary_to_octal_adhoc
Model: `chore: Rename Bin_to_octal.py to Conversions/binary_to_octal.py(# 5981)…`
Reference: `Update and rename bin_to_octal.py to binary_to_octal.py ()`
[Model](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=binary_to_octal_adhoc&choice=model) · [Reference](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=binary_to_octal_adhoc&choice=reference) · [Tie](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=binary_to_octal_adhoc&choice=tie) · [Skip](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=binary_to_octal_adhoc&choice=skip)
Files: 0 | +0/-0
Anchors: `bin_string`, `bin_to_octal.py`, `binary_to_octal.py`, `bin_string_in_3_list`, `bin_to_octal`

```diff
similarity index 96 % <nl> rename from conversions / bin_to_octal . py <nl> rename to conversions / binary_to_octal . py <nl> mmm a / conversions / bin_to_octal . py <nl> ppp b / conversions / binary_to_octal . py <nl> def bin_to_octal ( bin_string : str ) - > str : <nl> while len ( bin_string ) % 3 ! = 0 : <nl> bin_string = " 0 " + bin_string <nl> bin_string_in_3_list = [ <nl> - bin_string [ index : index + 3 ] <nl> + bin_string [ index : index + 3 ] <nl> for index , value in enumerate ( bin_string ) <nl> if index % 3 = = 0 <nl> ] <nl>
```