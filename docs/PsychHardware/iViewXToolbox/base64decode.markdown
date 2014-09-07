---
layout: mfile
title: base64decode
categories:
  - iViewXToolbox
encoding: UTF-8
---

BASE64DECODE Perform base64 decoding on a string.

   BASE64DECODE(STR) decodes the given base64 string STR.

   Any character not part of the 65-character base64 subset set is silently
   ignored.  Characters occuring after a '=' padding character are never
   decoded.

   STR doesn't have to be a string.  The only requirement is that it is a
   vector containing values in the range 0-255.

   If the length of the string to decode (after ignoring non-base64 chars) is
   not a multiple of 4, then a warning is generated.

   This function is used to decode strings from the Base64 encoding specified
   in RFC 2045 - MIME (Multipurpose Internet Mail Extensions).  The Base64
   encoding is designed to represent arbitrary sequences of octets in a form
   that need not be humanly readable.  A 65-character subset ([A-Za-z0-9+/=])
   of US-ASCII is used, enabling 6 bits to be represented per printable
   character.

   See also BASE64ENCODE.