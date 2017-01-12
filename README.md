Hiera eyaml
===========

This is a hacked version of https://github.com/TomPoulton/hiera-eyaml with https://github.com/dalen/puppet-puppetdbquery (v. 1.6.1, as this  it the last version working with Puppet 3.x which I am using as of now) embedded

Hiera entries like:

```
my::key: 'puppetdb:(Class["Myclass"]),fqdn'
```

...query PuppetDB, which returns array of `fqdn`s (fact) of nodes that are found using query `(Class["Myclass"])`.

See original projects for more info.
