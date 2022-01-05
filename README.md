# Fancy MOTD

Fancy, colorful MOTD written in bash. Server status at a glance.

![MOTD screenshot](readme-img.png)

## Usage
To see the output just run `motd.sh`. This runs all the scripts in `modules`
directory in order, `run-parts` style, and formats the output. One way to run
it at each login is to add a line to `~/.profile` file:

Need to load at /opt/motd

```
vim /etc/profile

bash /opt/motd/motd.sh
. /etc/ini.d/msm_profile
```

To add a new module you can create a new script in `modules`. For the output to
be properly formatted it has to use `print_columns` function from
`framework.sh`, please refer to the existing modules.

## Credits
Fancy MOTD is hugely inspired by [this repo](https://github.com/HermannBjorgvin/MOTD) by Hermann Björgvin.
