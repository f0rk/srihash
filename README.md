srihash - generate Subresource Integrity Digests from the command line
======================================================================

Subresource Integrity is a browser feature that allows you to specify the hash
of a resource being loaded by your webpage. This allows you to more safely use
CDN-distributed content. For more information, see
(Subresource Integrity on MDN)[https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity].

Usage
=====

```bash
~$ srihash https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css
sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7

~$ srihash validator.min.js
sha384-rL4GxM2e1/80hvGv4D2buQErmXQZi3AjwzlJe/znZjBf0KPfIUydKpSi38QVkzY/
```

You can then add the `integrity` attribute to your tags like so:
    
```html
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" type="text/css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">
<script type="text/javascript" src="validator.min.js" integrity="sha384-rL4GxM2e1/80hvGv4D2buQErmXQZi3AjwzlJe/znZjBf0KPfIUydKpSi38QVkzY/" crossorigin="anonymous"></script>
```

Installation
============

Copy the file `srihash` to your `bin` location of choice. Requires the `bash`,
`curl` or `wget`, and `opensl` commands to be installed.
