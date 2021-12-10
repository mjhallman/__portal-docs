[@jorsek/content-portal-configs](../README.md) / [Exports](../modules.md) / IAuthStrategy

# Interface: IAuthStrategy

**`description`** Authentication Strategy configuration object. Most fields are es6-syntax templatable with all values
defined on this object available to be used in other string fields and steps.

## Table of contents

### Properties

- [aud](iauthstrategy.md#aud)
- [authSigningKey](iauthstrategy.md#authsigningkey)
- [auth\_success\_redirect](iauthstrategy.md#auth_success_redirect)
- [auth\_uri](iauthstrategy.md#auth_uri)
- [client\_id](iauthstrategy.md#client_id)
- [client\_secret](iauthstrategy.md#client_secret)
- [grant\_type](iauthstrategy.md#grant_type)
- [hd](iauthstrategy.md#hd)
- [idp](iauthstrategy.md#idp)
- [iss](iauthstrategy.md#iss)
- [jwt\_key](iauthstrategy.md#jwt_key)
- [redirect\_path](iauthstrategy.md#redirect_path)
- [response\_type](iauthstrategy.md#response_type)
- [scope](iauthstrategy.md#scope)
- [steps](iauthstrategy.md#steps)

## Properties

### aud

• `Optional` **aud**: *string*

**`description`** Identity Provider Audience field to verify on JWT tokens.

Defined in: [types.d.ts:503](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L503)

___

### authSigningKey

• `Optional` **authSigningKey**: *string*

**`description`** Authentication signing key.
This can be created in easyDita and is a pre-shared key to create individualized tokens for each user.

Defined in: [types.d.ts:558](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L558)

___

### auth\_success\_redirect

• `Optional` **auth\_success\_redirect**: *string*

**`description`** Redirect path for when authenitcation is fully successful.

**`param`** Used to keep track of originally requested URL.

**`default`** "/?state=${state}"

Defined in: [types.d.ts:540](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L540)

___

### auth\_uri

• `Optional` **auth\_uri**: *string*

**`description`** URI to redirect to when the user needs authentication. any parameters returned on the incoming redirect back are available to the auth "steps" as "auth".
For example, if the first step requires the "code", you can construct the first step uri with ${auth.code} as
"https://some-idp/token?code=${auth.code}&client_id=${client_id}&client_secret=${client_secret}&redirect_uri=${base_uri}${redirect_path}&grant_type=${grant_type}&state=${state}",

**`example`** 

```json
{
  "auth_uri":"https://accounts.google.com/o/oauth2/auth?redirect_uri=${base_uri}${redirect_path}&client_id=${client_id}&response_type=${response_type}&scope=${scope}&state=${state}"
}
```

Defined in: [types.d.ts:553](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L553)

___

### client\_id

• `Optional` **client\_id**: *string*

**`description`** Identity Provider Client ID/ApplicationID for API requests.

Defined in: [types.d.ts:495](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L495)

___

### client\_secret

• `Optional` **client\_secret**: *string*

**`description`** Identity Provider Client Secret for API requests.

Defined in: [types.d.ts:499](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L499)

___

### grant\_type

• `Optional` **grant\_type**: *string*

**`description`** Identity Provider grant_type.

**`default`** "authorization_code"

Defined in: [types.d.ts:512](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L512)

___

### hd

• `Optional` **hd**: *string*[]

**`description`** Identity Provider HD/domain field to validate against.

Defined in: [types.d.ts:525](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L525)

___

### idp

• **idp**: *okta* \| *azure* \| *google* \| *keycloak* \| *custom* \| *jwt*

**`description`** Identity Provider Type.

Defined in: [types.d.ts:491](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L491)

___

### iss

• `Optional` **iss**: *string*

**`description`** Identity Provider Issuer field to verify on JWT tokens.

Defined in: [types.d.ts:507](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L507)

___

### jwt\_key

• `Optional` **jwt\_key**: *string*

**`description`** JWT field to use in cookies and to match on the steps to find the correct JWT step.

**`default`** "jwt"

Defined in: [types.d.ts:530](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L530)

___

### redirect\_path

• `Optional` **redirect\_path**: */auth/google*

**`description`** Redirect path for incoming oauth redirect from the IDP containing the grant_type.

Defined in: [types.d.ts:534](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L534)

___

### response\_type

• `Optional` **response\_type**: *string*

**`description`** Identity Provider response_type.

**`default`** "code"

Defined in: [types.d.ts:517](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L517)

___

### scope

• `Optional` **scope**: *https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/userinfo.email*

**`description`** Identity Provider oauth scopes.

Defined in: [types.d.ts:521](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L521)

___

### steps

• `Optional` **steps**: [*IAuthStrategyStep*](iauthstrategystep.md)[]

**`description`** Authenitcation steps. Run sequentially during authentication flow.

**`see`** IAuthStrategyStep

Defined in: [types.d.ts:563](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L563)
