# Gizber Barcode Specification

## Barcode Type

we use [PDF417](https://en.wikipedia.org/wiki/PDF417) for the pdf type, Please remember to add the gizber logo at the
left side of the barcode as a part of the
barcode

## Barcode Content

we use the [Csv Format](https://datatracker.ietf.org/doc/html/rfc4180) for a one line with the below keys and values

### Value types

#### Booleans

t = True    
f = False

#### Numbers

any number

#### Strings

anything else

### Available Keys

| Key | Definition           | Value Type |
|-----|----------------------|------------|
| o   | Organization Id      | number     |
| k   | Kippa Id             | number     |
| a   | amount               | number     |
| c   | custom               | string     |
| l   | Lock amount          | boolean    |
| dr  | Disable Recurring    | boolean    |
| di  | Disable Installments | boolean    |
| p   | Phone Number         | string     |
| fn  | first name           | string     |
| ln  | lest name            | string     |
| ad  | address              | string     |
| cm  | Comment              | string     |
| e   | email                | string     |
| er  | send email receipt   | boolean    |
| fnr | First name Required  | boolean    |
| lnr | Lest name Required   | boolean    |   
| adr | Address Required     | boolean    |   
| cmr | Comment required     | boolean    |   
| er  | Email  Required      | boolean    |   

organization id or kippa id is required, if you use kippa id than organization id will be ignored,
if you omit kippa id than donation will go directly to organization with no kupa.   
everything else is optional




    