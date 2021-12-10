[@jorsek/content-portal-configs](../README.md) / [Exports](../modules.md) / IAuthStrategyStep

# Interface: IAuthStrategyStep

**`description`** The authentication steps to make during the authentication flow.
This typically consists of a series of API calls to endpoints such as /token, /introspect, or /tokeninfo to
acquire information about the user and validate their tokens. See individual IDP documentation for more information

**`example`** 
```json
[
{
"name": "token",
"uri": "https://oauth2.googleapis.com/token?code=${auth.code}&client_id=${client_id}&client_secret=${client_secret}&redirect_uri=${base_uri}${redirect_path}&grant_type=${grant_type}&state=${state}",
"method": "POST",
"config": {
"headers": {
"Content-Type": "application/x-www-form-urlencoded"
}
}
},
{
"name": "jwt",
"uri": "https://www.googleapis.com/oauth2/v3/tokeninfo?id_token=${token.id_token}"
}
]
```

## Table of contents

### Properties

- [config](iauthstrategystep.md#config)
- [decode](iauthstrategystep.md#decode)
- [map](iauthstrategystep.md#map)
- [method](iauthstrategystep.md#method)
- [name](iauthstrategystep.md#name)
- [params](iauthstrategystep.md#params)
- [uri](iauthstrategystep.md#uri)

## Properties

### config

• `Optional` **config**: [*IJSONObject*](ijsonobject.md)

**`description`** Axios request config object.
NOTE: No options that are functions may be used here, only JSON.

**`see`** https://github.com/axios/axios#request-config

**`default`** {}

**`example`** 
```json
{ "headers": { "Content-Type": "application/x-www-form-urlencoded"} }
```

Defined in: [types.d.ts:663](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L663)

___

### decode

• `Optional` **decode**: *${token.id_token}*

**`description`** If provided, the step will attempt to JWT decode the value defined.
Typically this would be used in lieu of an /introspect endpoint if the previous
step returns a value as one of its properties.

**`default`** null

**`example`** <caption>our default keylcloak config</caption>

```json
[
{
"name": "token",
"uri": "${auth_endpoint}/token",
"method": "POST",
"params": {
"redirect_uri": "${base_uri}${redirect_path}",
"client_id": "${client_id}",
"code": "${auth.code}",
"grant_type": "authorization_code"
},
"config": {
"headers": {
"Content-Type": "application/x-www-form-urlencoded"
}
}
},
{
"name": "jwt",
"decode": "${token.id_token}"
}
]
```

Defined in: [types.d.ts:634](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L634)

___

### map

• **map**: *object*

**`description`** maps the response to different object key/value pairs so that if the IDP returns with different
values in the response from what you would otherwise put as keys in the resulting object, you can map them here.

**`default`** null

**`example`** 
```json
{
"map": {
"id_type": "typ",
"http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress": "email",
"http://schemas.xmlsoap.org/ws/2005/05/identity/claims/expiration": "exp"
}
}
 ```

#### Type declaration:

Defined in: [types.d.ts:679](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L679)

___

### method

• `Optional` **method**: *POST* \| *GET* \| *PUT*

**`description`** the method to use with the request uri

**`default`** GET

Defined in: [types.d.ts:645](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L645)

___

### name

• **name**: *string*

**`description`** the name of the flow step. any data returned by this step can be used in further template strings
with this name. for example, step2 may need information from step1 in the request uri and can be set as follows:
"https://some-idp.com/oauth2/v3/tokeninfo?id_token=${step1.id_token}".
If the step name is "jwt", or matches the "jwt_key" defined in the IAuthStrategy object, we will automatically
validate it.

**`default`** step${index}

**`example`** "step1", "step2"

Defined in: [types.d.ts:600](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L600)

___

### params

• `Optional` **params**: [*IJSONObject*](ijsonobject.md)

**`description`** any additional params to pass with the request.
NOTE: No options that are functions may be used here, only JSON.

**`see`** https://github.com/axios/axios#request-config

**`default`** {}

Defined in: [types.d.ts:652](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L652)

___

### uri

• **uri**: *string*

**`description`** the URI to make an api request

**`example`** 
"https://oauth2.googleapis.com/token?code=${auth.code}&client_id=${client_id}&client_secret=${client_secret}&redirect_uri=${base_uri}${redirect_path}&grant_type=${grant_type}&state=${state}",

Defined in: [types.d.ts:640](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L640)
