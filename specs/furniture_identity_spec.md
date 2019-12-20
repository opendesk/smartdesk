# Smartdesk Furniture Identity Spec

This document describes how identity is assigned to furniture to facilitate integration of technology. For clarity it uses specific key words such as SHOULD, MAY etc to describe its specifications, their meanings are given [here](key_word_definitions.md).

### Overview

There are many different way to identify objects in the real world and refer to them from within computer systems or databases. As a design principle for smartdesk identity the presumption is made that there is no central authority for generation of names or ids, and no single domain is to be used to resolve identity. With this in mind these specs are deliberately on the loose side, but try to support useful best practices.

### Naming Authority

- A identifiable piece of furniture MUST declare a naming authority that has named it. 
- A naming authority is a domain name, with optional sub-domains, that is under the control of the person/s or organisation that has named the furniture. 
- This authority is a convention adopted directly from URN https://en.wikipedia.org/wiki/Uniform_Resource_Identifier authority but restricted to only using host names and not including userinfo, port or ip.

### Unique Names

- A piece of smartdesk furniture SHOULD have a unique identifier. 
- This identifier MUST be a string of not more than 128 characters using only lowercase ascii encoded unreserved characters described in [RFC 3986](http://tools.ietf.org/html/rfc3986#section-2.3). This means lowercase alphanumeric and the characters `-`  `.`  `_`  `~`. This restriction is to ensure that these identifiers can be used unescaped in URIs.
- There is no common form for these identifiers to help guarantee their uniqueness, thus there is no guarantee of their uniqueness, rather it is the responsibility of their the naming authority to choose a strategy that suits their needs.
- A unique identifier MAY be a [UUID](https://en.wikipedia.org/wiki/Universally_unique_identifier) something like this `de305d54-75b4-431b-adb2-eb6b9e546014`
- A unique identifer MAY be short and human readable e.g. `pauls-desk`
- A unique name MAY contain a representation of information about the nature of the object it names e.g. `pauls-desk` or `dsk-paul` but this information SHOULD NOT be relied on expected to carry semantic significance. 


### Type names

- Furniture MAY adopt one or more terms from a taxonomy of type names to help describe itself.
- Compound identifiers for desks that wish to reference type names SHOULD use URN style structuring of these identifiers rather than compound strings. https://en.wikipedia.org/wiki/Uniform_Resource_Identifier 
- Such type names SHOULD be common words (in any language, but with the restrictions on character and encodings)
- Such terms MUST follow the same rules as unique names but with the following additional restrictions: no numbers, no use of  `-`  `.`  `~`, so that only underscore is used to separate words. This is to make it as robust as possible through different systems.
- Type names OUGHT to be chosen from common sets of terms shared between organisations to aid interoperatibilty.
- If a specific shared taxonomy is being use it SHOULD be indicated.
- Taxonomy's of type names MAY provide aliases to types to support human readability. These aliases should allow any utf-8 encoded strings to support multiple languages and localised naming conventions e.g. `chair` > `russian:стул`, `acronym:CHR`. Such aliases should not be used in cannonical names.


### Roles and Structures

- Furniture like many objects are used by multiple groups/organisations and therefore single object MAY have multiple names representing its different roles.
- Roles within organisations SHOULD follow the type and instance naming conventions layed out above and SHOULD adopt URN style composition. Best practice to aid in interoperability between organisations is to keep such structures flat for identity of objects and then use graphs of linked objects to describe organisational or physical structure. 


### URIs and URLs for desks

- A uri SHOULD include a unique identifier for the furniture as described above and have the same authority.
- A uri MAY be a url too at which further information about the desk can be discovered, but it may also have a separate url.
- A url MAY offer, either directly or by reference,  an API endpoint to communicate with a smartdesk.
- A url MAY offer, either directly or by reference,  a webpage providing information about the furniture.
- A url MAY offer, either directly or by reference,  structured information in json or xml about the furniture.

### Pubic and Private keys

-  piece of smartdesk furniture MAY have its own public/private key pair to facilitate secure communication.


### Human and machine readable ids

- If piece of smartdesk furniture has either a unique identifier and/or a uri they SHOULD be given on the surface of the furniture in both human and machine readable form, ie in both text and something like a bar or QR code.
