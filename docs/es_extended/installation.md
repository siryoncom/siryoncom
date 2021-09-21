# Installation

Instructions on how to download and install the basics of **ES Extended**.

## Requirements

- [mysql-async](https://github.com/brouznouf/fivem-mysql-async)
- [async](https://github.com/esx-framework/async)

## Download

### Using Git

```
cd resources
git clone https://github.com/esx-framework/es_extended/tree/legacy [essential]/es_extended
git clone https://github.com/esx-framework/esx_menu_default [esx]/[ui]/esx_menu_default
git clone https://github.com/esx-framework/esx_menu_dialog [esx]/[ui]/esx_menu_dialog
git clone https://github.com/esx-framework/esx_menu_list [esx]/[ui]/esx_menu_list
```

### Manually

- Download https://github.com/esx-framework/es_extended/tree/legacy
- Put it in the `resource/[essential]` directory
- Download https://github.com/esx-framework/esx_menu_default/releases/latest
- Put it in the `resource/[esx]/[ui]` directory
- Download https://github.com/esx-framework/esx_menu_dialog/releases/latest
- Put it in the `resource/[esx]/[ui]` directory
- Download https://github.com/esx-framework/esx_menu_list/releases/latest
- Put it in the `resource/[esx]/[ui]` directory

## Install

- Import `es_extended.sql` in your database
- Configure your `server.cfg` to look like this

```
add_principal group.admin group.user
add_ace resource.es_extended command.add_ace allow
add_ace resource.es_extended command.add_principal allow
add_ace resource.es_extended command.remove_principal allow
add_ace resource.es_extended command.stop allow


start mysql-async
start es_extended

start esx_menu_default
start esx_menu_list
start esx_menu_dialog
```
