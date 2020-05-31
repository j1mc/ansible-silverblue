fonts
=====

Install custom fonts to `~/.local/share/fonts`


Role Variables
--------------

```yaml
all_users:              # this role can configure for one or more users
  - user: foo           # username
    homedir: /home/foo  # the home dir for the username

all_fonts:              # the fonts you want to install
  - RobotoMono          # the name of these fonts must match the name of the
  - SourceCodePro       # font directory
  - DejaVuSansMono
  - UbuntuMono
```

License
-------

GPLv3

Author Information
------------------

  * Tiago M. Vieira - [https://github.com/tvieira](https://github.com/tvieira)
  * Jim Campbell (jwcampbell@gmail.com)

