actify | Python virtual environments done right.
================================================


Installation
------------

```
sudo sh -c 'curl https://raw.githubusercontent.com/mrshannon/actify/master/actify > /usr/local/bin/actify'
sudo chmod +x /usr/local/bin/actify
```

Usage
-----

TODO


Frequently Asked Questions
--------------------------

**Why does `actify` require bash?**

The answer is simple, I wrote `actify` in a couple of hours and did not have
time to worry about POSIX compliance.  Rewritting `actify` for `sh` is
something I may consider in the future.

**Can I get the (<environment>) prompt in shells besides bash?**

Yes, but you will need to add some lines to your shell config.  See Sash Hart's
excelent documation on this at
[Vex Documentation](https://github.com/sashahart/vex#shell-prompts).

**Why use `actify` instead of sourcing the activate script in the virtualenv?**

Simple, `actify` does not mess with the ENVIRONMENT of your current shell.
When the called process, or invoked shell exits you will be returned to the
same shell you called `actify` from.

**Isn't `actify` the same as vex then?**

Yes, but `actify` is much simpler, it does not try manage your environments but
simply provides a way to activate these environments and thus is easier to
integrate into environments where others are using unmanaged virtual
environments.  In fact, `actify` owes much to Sasha Hart and his excellent
[Vex](https://github.com/sashahart/vex) tool.
