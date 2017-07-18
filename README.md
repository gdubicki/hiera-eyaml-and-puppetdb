Hiera-eyaml and data from PuppetDB
==================================

This is a hacked version of https://github.com/TomPoulton/hiera-eyaml with embedded https://github.com/dalen/puppet-puppetdbquery (v. 1.6.1, as this  it the last version working with Puppet 3.x which I am using as of now) to provide getting live data from PuppetDB as hiera data.

Hiera entries with a prefix `puppetdb:`, like:

```
my::key: 'puppetdb:(Class["Myclass"]),fqdn'
```

...query PuppetDB, which returns array of `fqdn`s (fact) of nodes that are found using query `(Class["Myclass"])`.

All other hiera entries are queried only using hiera-eyamls, which makes it fast.


See original projects for more info.
