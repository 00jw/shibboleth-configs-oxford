A few configs to make life easier

# Shibboleth 2.x

## shibboleth2.test.xml

Rename to shibboleth2.xml for use. For generating the metadata required for registration.
Be sure to add the correct entityID


## shibboleth2.production.xml

Rename to shibboleth2.xml for use. Add the correct entityID and supportContact attributes.

Config includes:
 - EPPN descoping
 - Oxford only metadata
 - Longer timeout

# Shibboleth 3.x

Example configs are named shibboleth3.test.xml and shibboleth3.production.xml. Still rename these to shibboleth2.xml. 

# shibtest/index.php

add to apache webroot and protect with

```
Alias /shibtest/ /path/to/shibtest/
<Location /shibtest/>
    AuthType shibboleth
    ShibRequestSetting requireSession 1
    Require valid-user
</Location>
```
