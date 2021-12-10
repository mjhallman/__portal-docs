[@jorsek/content-portal-configs](../README.md) / [Exports](../modules.md) / IRedirects

# Interface: IRedirects

**`description`** configuration object that describes redirecting paths that are requested to the application.
Redirect rules are processed in order of declaration and trigger on first match.

**`example`** <caption>Example of redirects object</caption>
```json
"redirects": {
   "pathRegExp": false, // default false for performance considerations.
   "queryRegExp": true, // default false for performance considerations.
   "vars": {
       "env.NODE_ENV": {
           "production": "Production",
           ".*": "Staging",
       },
       "basePath": "https://my.cdn.com/${NODE_ENV}"
   },
   "paths": {
       "/something": "https://www.kittenwar.com",
   },
   "query": {
       "\\?p=mfm-fwc&v=([3-9].[8-9].[1-9][7-9][0-9])&t=(.+)(&|$)": "${basePath}/FieldTime/${1}/index.html#cshid=${2}",
       "\\?p=mfm-fwc&v=([3-9].[8-9].[1-9][7-9][0-9])(&|$)": "${basePath}/FieldTime/${1}/index.html",
       "\\?p=mfm-fwc&v=(.+)&t=(.+)(&|$)": "${basePath}/mfm/fwc/${1}/Default.htm#cshid=${2}",
       "\\?p=mfm-fwc&v=(.+)(&|$)": "${basePath}/mfm/fwc/${1}/Default.htm",
       "\\?p=Vista&v=([6][1][7-9]).+&t=(.+?)(&|$)": "${basePath}/Vista/${1}0/Default.htm#cshid=${2}",
       "\\?p=Vista&v=([6][1][7-9]).+(&|$)": "${basePath}/Vista/${1}0/Default.htm",
       "\\?p=(.+)&v=(.+)&t=(.+)(&|$)": "${basePath}/${1}/${2}/Default.htm#cshid=${3}",
       "\\?p=(.+)&v=(.+)(&|$)": "${basePath}/${1}/${2}/Default.htm"
   }
}
```

## Table of contents

### Properties

- [pathRegExp](iredirects.md#pathregexp)
- [paths](iredirects.md#paths)
- [query](iredirects.md#query)
- [queryRegExp](iredirects.md#queryregexp)
- [vars](iredirects.md#vars)

## Properties

### pathRegExp

• `Optional` **pathRegExp**: *boolean*

**`description`** whether to use regular expressions for the paths or not.

**`default`** false

Defined in: [types.d.ts:1018](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L1018)

___

### paths

• `Optional` **paths**: *object*

**`description`** paths to redirect the browser when requested.

**`example`** 
```json
"paths": {
    "/kittens": "https://www.kittenwar.com",
}
```

#### Type declaration:

Defined in: [types.d.ts:1050](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L1050)

___

### query

• `Optional` **query**: *object*

**`description`** query string parameter redirects. must begin with "?" or "\?" in the case of regex.
All inclusive query parameters and must be ordered.

Given the following configuration, a request to
https://my.portal.easydita.com/?hello=world&foo=baz
would be redirected to https://mysite.com/world/index.html#foo=baz

However, a request to
https://my.portal.easydita.com/?foo=baz&hello=world
https://my.portal.easydita.com/?hello=world
would not be redirected.

**`example`** 
```json
 "redirects" {
     "vars": {
         "baseUrl": "https://mysite.com"
     },
    "query": {
        "\\?hello=(world|you)&foo=(ba[rz])": "${baseUrl}/${1}/index.html#foo=${2}",
    }
}
```

#### Type declaration:

Defined in: [types.d.ts:1077](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L1077)

___

### queryRegExp

• `Optional` **queryRegExp**: *boolean*

**`description`** whether to use regular expressions for the query or not.

**`default`** false

Defined in: [types.d.ts:1023](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L1023)

___

### vars

• `Optional` **vars**: *object*

**`description`** variables to be used in other parts of the paths and query strings
"env.*" values are pulled from specifically available environment variables related to EZD
and the running NODE environment. You can specify what value to use given the environment. .* matches anything.

**`example`** 
```json
 "vars": {
     "env.NODE_ENV": {
         "production": "Production",
         ".*": "Staging",
     },
 }
```

#### Type declaration:

Defined in: [types.d.ts:1038](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L1038)
