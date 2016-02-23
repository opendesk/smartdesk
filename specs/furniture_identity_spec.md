# Smartdesk Furniture Identity Spec

This document describes how identity is assigned to furniture to facilitate integration of technology. For clarity it uses specific key words such as SHOULD, MAY etc to describe its specifications, their meanings are given [here](key_word_definitions.md).

### Overview

There are many different way to identify objects in the real world and refer to them from within computer systems or databases. As a design principle for smartdesk identity the presumption is made that there is no central authority for generation of names or ids, and no single domain is to be used to resolve identity. With this in mind these specs are deliberately on the loose side, but try to support useful best practices.


### Unique Identifiers

- A piece of smartdesk furniture MAY have a unique identifier. 
- This identifier MUST be a string of not more than 128 characters using only lowercase ascii encoded unreserved characters described in [RFC 3986](http://tools.ietf.org/html/rfc3986#section-2.3). This means lowercase alphanumeric and the characters `-`  `.`  `_`  `~`. This restriction is to ensure that these identifiers can be used unescaped in URIs.
- There is no common form for these identifiers to help guarantee their uniqueness, thus there is no guarantee of their uniqueness, rather it is the responsibility of their creator to choose a strategy that suits their needs.
- A unique identifier MAY be a [UUID](https://en.wikipedia.org/wiki/Universally_unique_identifier) something like this `de305d54-75b4-431b-adb2-eb6b9e546014`
- A unique identifier MAY use a domain either reversed or not to aid uniqueness eg `cc.opendesk.12345678`


### URIs and URLs

- A piece of smartdesk furniture MAY have a uri.
- A uri SHOULD include a unique identifier for the furniture as described above.
- A uri MAY be a url too at which further information about the desk can be discovered, but it may also have a separate url.
- A url MAY offer, either directly or by reference,  an API endpoint to communicate with a smartdesk.
- A url MAY offer, either directly or by reference,  a webpage providing information about the furniture.
- A url MAY offer, either directly or by reference,  structured information in json or xml about the furniture.


### Pubic and Private keys

-  piece of smartdesk furniture MAY have its own public/private key pair to facilitate secure communication.


### Human and machine readable ids

- If piece of smartdesk furniture has either a unique identifier and/or a uri they SHOULD be given on the surface of the furniture in both human and machine readable form, ie in both text and something like a bar or QR code.
