[@jorsek/content-portal-configs](../README.md) / [Exports](../modules.md) / IEzdEnv

# Interface: IEzdEnv

## Hierarchy

* **IEzdEnv**

  ↳ [*IEzdEnvOverride*](iezdenvoverride.md)

## Table of contents

### Properties

- [ANALYTICS\_APP\_ID](iezdenv.md#analytics_app_id)
- [ANALYTICS\_TOKEN](iezdenv.md#analytics_token)
- [DEPLOYMENT\_ID](iezdenv.md#deployment_id)
- [EZD\_CONFIG\_ENV](iezdenv.md#ezd_config_env)
- [EZD\_ENV](iezdenv.md#ezd_env)
- [EZD\_HOSTNAME](iezdenv.md#ezd_hostname)
- [EZD\_ORG](iezdenv.md#ezd_org)
- [EZD\_PORTAL\_CONFIG\_FILE](iezdenv.md#ezd_portal_config_file)
- [EZD\_TOKEN](iezdenv.md#ezd_token)
- [EZD\_URL\_SCHEME](iezdenv.md#ezd_url_scheme)
- [FIREBASE\_CONFIG](iezdenv.md#firebase_config)
- [GA\_TRACKING\_ID](iezdenv.md#ga_tracking_id)
- [GOOGLE\_PUBSUB\_ID](iezdenv.md#google_pubsub_id)
- [GTM\_TRACKING\_ID](iezdenv.md#gtm_tracking_id)
- [PORT](iezdenv.md#port)
- [ROOT\_MAP\_ID](iezdenv.md#root_map_id)

## Properties

### ANALYTICS\_APP\_ID

• `Optional` **ANALYTICS\_APP\_ID**: *string*

**`description`** Datadog analytics application id

Defined in: [types.d.ts:734](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L734)

___

### ANALYTICS\_TOKEN

• `Optional` **ANALYTICS\_TOKEN**: *string*

**`description`** Datadog analytics application token

Defined in: [types.d.ts:738](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L738)

___

### DEPLOYMENT\_ID

• `Optional` **DEPLOYMENT\_ID**: *string*

**`description`** easyDita deployment ID.

Defined in: [types.d.ts:762](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L762)

___

### EZD\_CONFIG\_ENV

• `Optional` **EZD\_CONFIG\_ENV**: *prod* \| *stg* \| *uat* \| *qa* \| *dev*

**`description`** the content-portal environment configuration key.
This lets the runtime know what configuration set to use from IPortalConfig

Defined in: [types.d.ts:715](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L715)

___

### EZD\_ENV

• `Optional` **EZD\_ENV**: *string*

**`description`** the easyDita environment to use

Defined in: [types.d.ts:706](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L706)

___

### EZD\_HOSTNAME

• **EZD\_HOSTNAME**: *string*

**`description`** the hostname of the easyDita api endpoint

Defined in: [types.d.ts:694](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L694)

___

### EZD\_ORG

• **EZD\_ORG**: *string*

**`description`** the org configured in easyDita

Defined in: [types.d.ts:690](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L690)

___

### EZD\_PORTAL\_CONFIG\_FILE

• `Optional` **EZD\_PORTAL\_CONFIG\_FILE**: *string*

**`description`** the content-portal configuration to use for the entire deployment.
this overrides the domain setting entirely when set for the Docker container.
This can either be a path to a file, or a base64-encoded string with the config.
This is not set in the configuration file, but set on the deployed container.

**`example`** <caption>URI to file</caption>
```sh
export EZD_PORTAL_CONFIG_FILE=./some_config.json
```

**`example`** <caption>base64 encoded.</caption>
```sh
export EZD_PORTAL_CONFIG_FILE=ewogICAgInRlbmFudCI6ICJqb3JzZWsiLAogICAgInRpdGxlIjogIkRldmVsb3BlciBHdWlkZSIsCiAgICAiZW52IjogewogICAgICAgICJFWkRfT1JHIjogImpvcnNlayIsCiAgICAgICAgIkVaRF9IT1NUTkFNRSI6ICJjb250ZW50LmVhc3lkaXRhLmNvbSIsCiAgICAgICAgIkVaRF9UT0tFTiI6ICJmYWtlLXRva2VuIiwKICAgICAgICAiUk9PVF9NQVBfSUQiOiAiMDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDAwMDAwMDQyIgogICAgfQp9
```

Defined in: [types.d.ts:730](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L730)

___

### EZD\_TOKEN

• **EZD\_TOKEN**: *string*

**`description`** easyDita API token.

Defined in: [types.d.ts:698](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L698)

___

### EZD\_URL\_SCHEME

• `Optional` **EZD\_URL\_SCHEME**: *http://* \| *https://*

**`description`** the hostname scheme to use for contacting the API.

Defined in: [types.d.ts:710](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L710)

___

### FIREBASE\_CONFIG

• `Optional` **FIREBASE\_CONFIG**: *string*

**`description`** base64 encoded json configuration for firebase.

Defined in: [types.d.ts:742](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L742)

___

### GA\_TRACKING\_ID

• `Optional` **GA\_TRACKING\_ID**: *string*

**`description`** The Google analytics tracking ID.

Defined in: [types.d.ts:754](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L754)

___

### GOOGLE\_PUBSUB\_ID

• `Optional` **GOOGLE\_PUBSUB\_ID**: *string*

**`description`** the subscription ID of PUB/SUB notifications to reload the configuration.

Defined in: [types.d.ts:746](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L746)

___

### GTM\_TRACKING\_ID

• `Optional` **GTM\_TRACKING\_ID**: *string*

**`description`** The Google Tag Manager tracking ID.

Defined in: [types.d.ts:758](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L758)

___

### PORT

• `Optional` **PORT**: *string*

**`description`** the port to run the express.js server on.

Defined in: [types.d.ts:750](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L750)

___

### ROOT\_MAP\_ID

• **ROOT\_MAP\_ID**: *string*

**`description`** easyDita root ditamap guid token.

Defined in: [types.d.ts:702](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L702)
