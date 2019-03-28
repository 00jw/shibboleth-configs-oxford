A few configs to make life easier

## shibboleth2.test.xml

Rename to shibboleth2.xml for use. For generating the metadata required for registration. Be sure to add the correct entityID
x

## shibboleth2.production.xml

Rename to shibboleth2.xml for use. Add the correct entityID and supportContact attributes.

Config includes:
 - EPPN descoping
 - Oxford only metadata
 - Longer timeout


## shibtest/index.php

add to apache webroot and protect with

```
Alias /shibtest/ /path/to/shibtest/
<Location /shibtest/>
    AuthType shibboleth
    ShibRequestSetting requireSession 1
    Require valid-user
</Location>
```
