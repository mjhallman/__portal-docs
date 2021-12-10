[@jorsek/content-portal-configs](../README.md) / [Exports](../modules.md) / IEzdEnvOverride

# Interface: IEzdEnvOverride

## Hierarchy

* [*IEzdEnv*](iezdenv.md)

  ↳ **IEzdEnvOverride**

## Table of contents

### Properties

- [ANALYTICS\_APP\_ID](iezdenvoverride.md#analytics_app_id)
- [ANALYTICS\_TOKEN](iezdenvoverride.md#analytics_token)
- [DEPLOYMENT\_ID](iezdenvoverride.md#deployment_id)
- [EZD\_CONFIG\_ENV](iezdenvoverride.md#ezd_config_env)
- [EZD\_ENV](iezdenvoverride.md#ezd_env)
- [EZD\_HOSTNAME](iezdenvoverride.md#ezd_hostname)
- [EZD\_ORG](iezdenvoverride.md#ezd_org)
- [EZD\_PORTAL\_CONFIG\_FILE](iezdenvoverride.md#ezd_portal_config_file)
- [EZD\_TOKEN](iezdenvoverride.md#ezd_token)
- [EZD\_URL\_SCHEME](iezdenvoverride.md#ezd_url_scheme)
- [FIREBASE\_CONFIG](iezdenvoverride.md#firebase_config)
- [GA\_TRACKING\_ID](iezdenvoverride.md#ga_tracking_id)
- [GOOGLE\_PUBSUB\_ID](iezdenvoverride.md#google_pubsub_id)
- [GTM\_TRACKING\_ID](iezdenvoverride.md#gtm_tracking_id)
- [PORT](iezdenvoverride.md#port)
- [ROOT\_MAP\_ID](iezdenvoverride.md#root_map_id)

## Properties

### ANALYTICS\_APP\_ID

• `Optional` **ANALYTICS\_APP\_ID**: *string*

**`description`** Datadog analytics application id

Inherited from: [IEzdEnv](iezdenv.md).[ANALYTICS_APP_ID](iezdenv.md#analytics_app_id)

Defined in: [types.d.ts:734](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L734)

___

### ANALYTICS\_TOKEN

• `Optional` **ANALYTICS\_TOKEN**: *string*

**`description`** Datadog analytics application token

Inherited from: [IEzdEnv](iezdenv.md).[ANALYTICS_TOKEN](iezdenv.md#analytics_token)

Defined in: [types.d.ts:738](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L738)

___

### DEPLOYMENT\_ID

• `Optional` **DEPLOYMENT\_ID**: *string*

**`description`** easyDita deployment ID.

Overrides: [IEzdEnv](iezdenv.md).[DEPLOYMENT_ID](iezdenv.md#deployment_id)

Defined in: [types.d.ts:785](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L785)

___

### EZD\_CONFIG\_ENV

• `Optional` **EZD\_CONFIG\_ENV**: *prod* \| *stg* \| *uat* \| *qa* \| *dev*

**`description`** the content-portal environment configuration key.
This lets the runtime know what configuration set to use from IPortalConfig

Inherited from: [IEzdEnv](iezdenv.md).[EZD_CONFIG_ENV](iezdenv.md#ezd_config_env)

Defined in: [types.d.ts:715](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L715)

___

### EZD\_ENV

• `Optional` **EZD\_ENV**: *string*

**`description`** the easyDita environment to use

Inherited from: [IEzdEnv](iezdenv.md).[EZD_ENV](iezdenv.md#ezd_env)

Defined in: [types.d.ts:706](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L706)

___

### EZD\_HOSTNAME

• `Optional` **EZD\_HOSTNAME**: *string*

**`description`** the hostname of the easyDita api endpoint

Overrides: [IEzdEnv](iezdenv.md).[EZD_HOSTNAME](iezdenv.md#ezd_hostname)

Defined in: [types.d.ts:773](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L773)

___

### EZD\_ORG

• `Optional` **EZD\_ORG**: *string*

**`description`** the org configured in easyDita

Overrides: [IEzdEnv](iezdenv.md).[EZD_ORG](iezdenv.md#ezd_org)

Defined in: [types.d.ts:769](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L769)

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

Inherited from: [IEzdEnv](iezdenv.md).[EZD_PORTAL_CONFIG_FILE](iezdenv.md#ezd_portal_config_file)

Defined in: [types.d.ts:730](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L730)

___

### EZD\_TOKEN

• `Optional` **EZD\_TOKEN**: *string*

**`description`** easyDita API token.

Overrides: [IEzdEnv](iezdenv.md).[EZD_TOKEN](iezdenv.md#ezd_token)

Defined in: [types.d.ts:777](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L777)

___

### EZD\_URL\_SCHEME

• `Optional` **EZD\_URL\_SCHEME**: *http://* \| *https://*

**`description`** the hostname scheme to use for contacting the API.

Inherited from: [IEzdEnv](iezdenv.md).[EZD_URL_SCHEME](iezdenv.md#ezd_url_scheme)

Defined in: [types.d.ts:710](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L710)

___

### FIREBASE\_CONFIG

• `Optional` **FIREBASE\_CONFIG**: *string*

**`description`** base64 encoded json configuration for firebase.

Inherited from: [IEzdEnv](iezdenv.md).[FIREBASE_CONFIG](iezdenv.md#firebase_config)

Defined in: [types.d.ts:742](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L742)

___

### GA\_TRACKING\_ID

• `Optional` **GA\_TRACKING\_ID**: *string*

**`description`** The Google analytics tracking ID.

Inherited from: [IEzdEnv](iezdenv.md).[GA_TRACKING_ID](iezdenv.md#ga_tracking_id)

Defined in: [types.d.ts:754](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L754)

___

### GOOGLE\_PUBSUB\_ID

• `Optional` **GOOGLE\_PUBSUB\_ID**: *string*

**`description`** the subscription ID of PUB/SUB notifications to reload the configuration.

Inherited from: [IEzdEnv](iezdenv.md).[GOOGLE_PUBSUB_ID](iezdenv.md#google_pubsub_id)

Defined in: [types.d.ts:746](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L746)

___

### GTM\_TRACKING\_ID

• `Optional` **GTM\_TRACKING\_ID**: *string*

**`description`** The Google Tag Manager tracking ID.

Inherited from: [IEzdEnv](iezdenv.md).[GTM_TRACKING_ID](iezdenv.md#gtm_tracking_id)

Defined in: [types.d.ts:758](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L758)

___

### PORT

• `Optional` **PORT**: *string*

**`description`** the port to run the express.js server on.

Inherited from: [IEzdEnv](iezdenv.md).[PORT](iezdenv.md#port)

Defined in: [types.d.ts:750](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L750)

___

### ROOT\_MAP\_ID

• `Optional` **ROOT\_MAP\_ID**: *string*

**`description`** easyDita root ditamap guid token.

Overrides: [IEzdEnv](iezdenv.md).[ROOT_MAP_ID](iezdenv.md#root_map_id)

Defined in: [types.d.ts:781](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L781)
