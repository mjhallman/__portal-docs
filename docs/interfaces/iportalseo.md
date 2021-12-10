[@jorsek/content-portal-configs](../README.md) / [Exports](../modules.md) / IPortalSeo

# Interface: IPortalSeo

# SEO

Seo is automatically handled by the base image in conjunction with the customer configuration.

`/robots.txt` allows everything except for /api routes to be crawled.

`/sitemap.xml` is generated automatically by the sitemap structure returned from the content API. 

The root `sitemap.xml` contains the `sitemapindex` xml definition [see sitemaps.org for more details](https://sitemaps.org)

Every `sitesection` defined in the easyDita root map generates a `sitemap` entry in the root `sitemap.xml`

The `loc` property for those entries is the `sitesecton.href` + `/sitemap.xml`. 

Example: `https://jorsek-portal.easydita.com/sitemap.xml` contains an entry for `https://jorsek-portal.easydita.com/guides/sitemap.xml`. The `/guides/sitemap.xml` is the one that contains the `urlset` for the `/guides/*` parts of the site.

The `canonical url` is set automatically by the request domain.

### Customer configuration variables for SEO

The configuration has the following variables for SEO purposes: 

```json
{
    "title": "EZD Content Help",
    "description": "Some descriptive text",
    "keywords": [ "special","keywords","defined by tenant"],
    "seo": {
        "sitemapUrlset": ["https://my.custom.domain/sitemap.xml"],
        "sitemapChangefreq": "monthly",
        "title": "EZD Content Help",
        "description": "Some descriptive text",
        "keywords": [ "special","keywords","defined by tenant"]
    }
}
```

The `seo` field takes precedence. Then, falls back to the root `title`, `description`, and `keywords`.

`<title>`, `<description>`, and `<keywords>` are also handled on a per `sitesection` and `content` page basis. 
Those will override globally defined defaults in the config.

## Table of contents

### Properties

- [description](iportalseo.md#description)
- [keywords](iportalseo.md#keywords)
- [sitemapChangefreq](iportalseo.md#sitemapchangefreq)
- [sitemapUrlset](iportalseo.md#sitemapurlset)
- [title](iportalseo.md#title)

## Properties

### description

• `Optional` **description**: *string*

**`description`** The default HTML description for the site.

Defined in: [types.d.ts:927](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L927)

___

### keywords

• `Optional` **keywords**: *string*[]

**`description`** The default keywords used for SEO purposes.

Defined in: [types.d.ts:931](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L931)

___

### sitemapChangefreq

• `Optional` **sitemapChangefreq**: *always* \| *hourly* \| *daily* \| *weekly* \| *monthly* \| *yearly* \| *never*

**`description`** The change frequency to set for the site. Used for SEO purposes.

Defined in: [types.d.ts:939](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L939)

___

### sitemapUrlset

• `Optional` **sitemapUrlset**: *string*[]

**`description`** The any additional sitemap.xml urls to include in the output for sitemap.xml. Used for SEO purposes.

Defined in: [types.d.ts:935](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L935)

___

### title

• `Optional` **title**: *string*

**`description`** The default HTML title for the site.

Defined in: [types.d.ts:923](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L923)
