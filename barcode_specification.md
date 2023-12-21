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

| Key | Definition                   | Value Type      |
|-----|------------------------------|-----------------|
| o   | Organization Id              | number          |
| k   | Kippa Id                     | number          |
| a   | amount                       | number          |
| l   | Lock amount                  | boolean         |
| ma  | Minimum Amount               | number          |
| dr  | Disable Recurring            | boolean         |
| rc  | Recurring Count              | number          |
| rf  | Recurring Frequency          | `d` `w` `m` `y` |
| di  | Disable Installments         | boolean         |
| im  | Installments Months          | number          |
| mim | Maximum Installments Months  | number          |
| do  | Default Open Option          | `o` `r` `i`     |
| p   | Phone Number                 | string          |
| fn  | first name                   | string          |
| ln  | lest name                    | string          |
| ad  | address                      | string          |
| cm  | Comment                      | string          |
| e   | email                        | string          |
| ser | send email receipt           | boolean         |
| fns | First Name Suggest           | boolean         |
| fnr | First name Required          | boolean         |
| lns | Lest Name suggest            | boolean         |
| lnr | Lest name Required           | boolean         |   
| ads | Address Suggest              | boolean         |
| adr | Address Required             | boolean         |   
| cms | Command Suggest              | boolean         |
| cmr | Comment required             | boolean         |   
| es  | Email Suggest                | boolean         |
| er  | Email  Required              | boolean         |   
| c   | custom                       | string          |

organization id or kippa id is required, if you use kippa id than organization id will be ignored,
if you omit kippa id than donation will go directly to organization with no kupa.   
everything else is optional

`rf` Recurring frequency: is `d` for daily, `w` for weekly, `m` for monthly and `y` for yearly

`do` Default open option: is `o` for one-time, `r` for recurring and `i` for installments



    