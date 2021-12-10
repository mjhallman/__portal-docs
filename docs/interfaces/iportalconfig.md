[@jorsek/content-portal-configs](../README.md) / [Exports](../modules.md) / IPortalConfig

# Interface: IPortalConfig

**`interface`** IPortalConfig

**`description`** Tenant configuration for a content-portal deployment.

**`example`** <caption>as a JSON file with minimum configuration</caption>
```json
{
   "env": {
       "EZD_ORG": "jorsek-docs",
       "EZD_HOSTNAME": "content-dev.easydita.com",
       "EZD_TOKEN": "{api-token}",
       "ROOT_MAP_ID": "4e8f5350-65f9-11eb-8765-02428d90e38c"
   }
}
```

**`example`** <caption>as a *.{js/ts} file</caption>
```json
const config = (): IPortalConfig => ({
   "env": {
       "EZD_ORG": "jorsek-docs",
       "EZD_HOSTNAME": "content-dev.easydita.com",
       "EZD_TOKEN": "{api_token}",
       "ROOT_MAP_ID": "4e8f5350-65f9-11eb-8765-02428d90e38c"
   }
})
```

export default config;

## Table of contents

### Properties

- [JSSInjectFirst](iportalconfig.md#jssinjectfirst)
- [allowTranslations](iportalconfig.md#allowtranslations)
- [analytics](iportalconfig.md#analytics)
- [authRequired](iportalconfig.md#authrequired)
- [authStrategy](iportalconfig.md#authstrategy)
- [cacheExpiry](iportalconfig.md#cacheexpiry)
- [defaultSectionIcon](iportalconfig.md#defaultsectionicon)
- [description](iportalconfig.md#description)
- [disableLocaleDate](iportalconfig.md#disablelocaledate)
- [disableSEO](iportalconfig.md#disableseo)
- [domain](iportalconfig.md#domain)
- [env](iportalconfig.md#env)
- [env.dev](iportalconfig.md#env.dev)
- [env.local](iportalconfig.md#env.local)
- [env.prod](iportalconfig.md#env.prod)
- [env.qa](iportalconfig.md#env.qa)
- [env.stg](iportalconfig.md#env.stg)
- [env.uat](iportalconfig.md#env.uat)
- [ezdSitemapConfig](iportalconfig.md#ezdsitemapconfig)
- [favicon](iportalconfig.md#favicon)
- [footer](iportalconfig.md#footer)
- [groups](iportalconfig.md#groups)
- [i18n](iportalconfig.md#i18n)
- [keywords](iportalconfig.md#keywords)
- [knownIssuesUrl](iportalconfig.md#knownissuesurl)
- [manifest](iportalconfig.md#manifest)
- [noSSR](iportalconfig.md#nossr)
- [outputClasses](iportalconfig.md#outputclasses)
- [permalinkFormat](iportalconfig.md#permalinkformat)
- [prerenderToc](iportalconfig.md#prerendertoc)
- [prettifyCode](iportalconfig.md#prettifycode)
- [prettifyCodeLang](iportalconfig.md#prettifycodelang)
- [prettifyCopyBadge](iportalconfig.md#prettifycopybadge)
- [prettifyGlobalLineNumbers](iportalconfig.md#prettifygloballinenumbers)
- [prettifyLineNumberDecorator](iportalconfig.md#prettifylinenumberdecorator)
- [prettifyPre](iportalconfig.md#prettifypre)
- [prettifySelector](iportalconfig.md#prettifyselector)
- [prettifyTheme](iportalconfig.md#prettifytheme)
- [redirects](iportalconfig.md#redirects)
- [relatedResources](iportalconfig.md#relatedresources)
- [scripts](iportalconfig.md#scripts)
- [search](iportalconfig.md#search)
- [sectionFilter](iportalconfig.md#sectionfilter)
- [seo](iportalconfig.md#seo)
- [stylesheets](iportalconfig.md#stylesheets)
- [supportedBrowserMinimumVersions](iportalconfig.md#supportedbrowserminimumversions)
- [tenant](iportalconfig.md#tenant)
- [theme](iportalconfig.md#theme)
- [title](iportalconfig.md#title)
- [toc](iportalconfig.md#toc)
- [unsupportedBrowserFile](iportalconfig.md#unsupportedbrowserfile)
- [unsupportedBrowserRegExp](iportalconfig.md#unsupportedbrowserregexp)
- [webFonts](iportalconfig.md#webfonts)

## Properties

### JSSInjectFirst

• `Optional` **JSSInjectFirst**: *boolean*

**`description`** controls the injectFirst property of the JSS client-side style renderer.

Defined in: [types.d.ts:443](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L443)

___

### allowTranslations

• `Optional` **allowTranslations**: *boolean*

Defined in: [types.d.ts:479](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L479)

___

### analytics

• `Optional` **analytics**: [*IPortalAnalytics*](iportalanalytics.md)

**`memberof`** IPortalConfig

**`description`** analytics configuration flags.
[IPortalAnalytics](iportalanalytics.md)

Defined in: [types.d.ts:236](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L236)

___

### authRequired

• `Optional` **authRequired**: *boolean*

**`description`** whether or not authentication is required.

Defined in: [types.d.ts:429](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L429)

___

### authStrategy

• `Optional` **authStrategy**: [*IAuthStrategy*](iauthstrategy.md) \| [*IAuthStrategy*](iauthstrategy.md)[]

**`description`** Authentication Strategy to use.

Defined in: [types.d.ts:434](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L434)

___

### cacheExpiry

• `Optional` **cacheExpiry**: *number*

**`description`** How long in seconds to set the Cache-Control header.

Defined in: [types.d.ts:425](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L425)

___

### defaultSectionIcon

• `Optional` **defaultSectionIcon**: *string*

**`description`** the default Icon to display for site sections.
This can be configured within the sitemap in easyDita per site section.

**`example`** 
```json
"defaultSectionIcon": "https://my.favorite.cdn/default-icon.png",
```

Defined in: [types.d.ts:110](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L110)

___

### description

• `Optional` **description**: *string*

**`description`** The default HTML description for the site.

Defined in: [types.d.ts:89](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L89)

___

### disableLocaleDate

• `Optional` **disableLocaleDate**: *boolean*

Defined in: [types.d.ts:478](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L478)

___

### disableSEO

• `Optional` **disableSEO**: *boolean*

**`memberof`** IPortalConfig

**`description`** Disables SEO crawling through robots meta and robots.txt

**`default`** false

Defined in: [types.d.ts:242](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L242)

___

### domain

• `Optional` **domain**: *string*[]

**`description`** a regular expression string|string[] to activate based on the domain. Domains MUST be unique.
When a request to the content portal server comes through a domain that matches anything in the list,
This configuration will be the one that is active.

**`default`** By default, we test the name of the tenant itself against the domain if this is omitted.

**`example`** <caption>configuring multiple domains.</caption>
```json
"domain": ["docs.jorsek.com", "jorsek(dev|qa|uat|stg)?-?.(portal|sites).easydita.com"]
```

Defined in: [types.d.ts:56](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L56)

___

### env

• **env**: [*IEzdEnv*](iezdenv.md)

**`description`** Default runtime environment variables
[IEzdEnv](iezdenv.md)

Defined in: [types.d.ts:151](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L151)

___

### env.dev

• `Optional` **env.dev**: [*IEzdEnvOverride*](iezdenvoverride.md)

**`description`** Default runtime environment variables for EZD_CONFIG_ENV=dev
[IEzdEnv](iezdenv.md)

Defined in: [types.d.ts:156](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L156)

___

### env.local

• `Optional` **env.local**: [*IEzdEnvOverride*](iezdenvoverride.md)

**`description`** Default runtime environment variables for EZD_CONFIG_ENV=local
[IEzdEnv](iezdenv.md)

Defined in: [types.d.ts:151](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L151)

___

### env.prod

• `Optional` **env.prod**: [*IEzdEnvOverride*](iezdenvoverride.md)

**`description`** Default runtime environment variables for EZD_CONFIG_ENV=prod
[IEzdEnv](iezdenv.md)

Defined in: [types.d.ts:176](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L176)

___

### env.qa

• `Optional` **env.qa**: [*IEzdEnvOverride*](iezdenvoverride.md)

**`description`** Default runtime environment variables for EZD_CONFIG_ENV=qa
[IEzdEnv](iezdenv.md)

Defined in: [types.d.ts:161](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L161)

___

### env.stg

• `Optional` **env.stg**: [*IEzdEnvOverride*](iezdenvoverride.md)

**`description`** Default runtime environment variables for EZD_CONFIG_ENV=stg
[IEzdEnv](iezdenv.md)

Defined in: [types.d.ts:171](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L171)

___

### env.uat

• `Optional` **env.uat**: [*IEzdEnvOverride*](iezdenvoverride.md)

**`description`** Default runtime environment variables for EZD_CONFIG_ENV=uat
[IEzdEnv](iezdenv.md)

Defined in: [types.d.ts:166](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L166)

___

### ezdSitemapConfig

• `Optional` **ezdSitemapConfig**: *boolean*

**`description`** flag to tell the system whether or not to always pull a config from easydita

Defined in: [types.d.ts:447](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L447)

___

### favicon

• `Optional` **favicon**: *string*

**`description`** Favicon url. Can be a *.ico or *.png file.

**`example`** 
```json
"favicon": "https://my.favorite.cdn/favicon.ico",
```

Defined in: [types.d.ts:101](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L101)

___

### footer

• `Optional` **footer**: [*IPortalFooter*](iportalfooter.md)

**`description`** footer configuration options.
[IPortalFooter](iportalfooter.md)

Defined in: [types.d.ts:146](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L146)

___

### groups

• `Optional` **groups**: *object*

#### Type declaration:

Defined in: [types.d.ts:480](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L480)

___

### i18n

• `Optional` **i18n**: *object*

**`description`** i18n string overrides for the application.

**`example`** <caption>By default, it's a simple key-value pair. However, there are reserved keywords, including `${page}`, which allows users to designate different text for a given key based on the page. `index-root` designates the home page, the rest of the pages are designated by `{pageName}-index`, such as `search-index`, for example.</caption>
```json
"message.hero.title": "${message.${page}.hero.title}",
"message.index-root.hero.title": "Welcome to the home page",
"message.section-index.hero.title": "Here's a section's landing page",
"message.content-index.hero.title": "This is the content page",
"message.search-index.hero.title": "Here are your search results",
"message.error-index.hero.title": "Looks like there's an error",
```

**`example`** <caption>There is also the reserved keyword `${@plural}`, as well, which can handle plural text options for a given sum. This is invoked via the property `count`, which can be passed into the`<I18nMessage>` component either as an individual `count: #` or through the `values` property object.<caption>
```json
"plural.0": "zero",
"plural.1": "one",
"plural.#": "any",
"message.search.results-found": "${message.search.results-found.${@plural}}",
"message.search.results-found.zero": "No results found",
"message.search.results-found.one": "One result found",
"message.search.results-found.any": "${@count} results found",
```

**`default`** 
```json
"i18n": {
"en-US": {
"label.tenant": "Jorsek",
"label.section": "Section",
"label.home": "Home",
"label.sections": "Sections",
"label.section-contents": "${label.section} ${label.contents}",
"label.contents": "Contents",
"label.filters": "Filters",
"label.related": "Related",
"label.resources": "Resources",
"label.articles": "Articles",
"label.featured": "Featured",
"label.filter": "Filter",
"label.filter.apply": "Apply ${label.filter}s",
"label.filter.clear": "Clear ${label.filter}",
"label.filter.results": "${label.filter} Results",
"label.result": "result",
"label.show-contents": "Show ${label.contents}",
"label.show-sections": "Show Page Sections",
"label.print": "Print page",
"label.print-sub": "${label.print} and subpages",
"label.last-updated": "Last updated: ${date}",
"label.related-resources": "${label.related} ${label.resources}",
"label.related-articles": "${label.related} ${label.articles}:",
"label.search.facet.Information_Type": "Information Type",
"label.search.facet.Area": "Area",
"label.search.facet.Mobile": "Mobile",
"label.featured-articles": "${label.featured} ${label.articles}",
"label.featured-videos": "${label.featured} Videos",
"label.whats-new": "What's New",
"label.version.prefix": "v ",
"label.version.format": "${title}",
"message.search.placeholder": "Search ${label.section} Help",
"message.search.results": "Search Results",
"message.missing-content": "[MISSING CONTENT]",
"plural.0": "zero",
"plural.1": "one",
"plural.#": "any",
"http.error.404": "not-found",
"http.error.#": "other",
"message.search.results-found": "${message.search.results-found.${@plural}}",
"message.search.results-found.zero": "No results found",
"message.search.results-found.one": "One result found",
"message.search.results-found.any": "${startIndex} - ${endIndex} of ${@count} results found",
"message.explore": "Explore Topics",
"message.hero.title": "Welcome to ${label.tenant}'s Help Portal",
"message.hero.sub-title": "Welcome to ${label.tenant}'s Help Portal",
"message.error.known-issues-link": "View known issues ",
"message.error.known-issues": "with the EZD Content Portal",
"message.error.status": "${message.error.status.${@http.error}}",
"message.error.next-steps": "${message.error.next-steps.${@http.error}}",
"message.error.status.not-found": "Sorry, we couldn't find that page.",
"message.error.status.other": "Sorry! Something seems to have broken on our end. An alert has been sent to the system admin.",
"message.error.next-steps.not-found": "You can select a topic to open the Help or use the search field.",
"message.error.next-steps.other": "You can select a topic to open the Help or use the search field.",
"message.search.result-found": "Search Results",
"message.browser.not-supported": "You seem to be using an unsupported browser.",
"message.browser.please-use": "To visit, please use one of the following browsers:",
"message.browser.links": "Use the links to download the latest version of a supported browser if you don't already have one installed.",
"message.browser.chrome": "Chrome",
"message.browser.firefox": "Firefox",
"message.browser.edge": "Edge",
"message.browser.safari": "Safari",
"message.footer.copyright": "Copyright: © 2021 Intellectual Property. All rights reserved.",
"message.chunked.title": "${content.title}",
"message.user.welcome": "${given_name}",
"message.user.login": "Login",
"message.user.logout": "Logout",
"message.login": "Please sign in.",
"message.logout.success": "You have been successfully logged out!",
"message.logout.login-again": "Sign in again",
"message.logout.sso-logout": "Sign out of SSO",
"message.logout.redirect": "This page will redirect in ${delay} seconds...",
"message.select.version": "${selectedVersion}",
"message.notification-banner.link-text": "Send us your feedback",
"message.notification-banner.text": "&nbspon the new site. We appreciate it."
}
}
```

#### Type declaration:

Defined in: [types.d.ts:352](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L352)

___

### keywords

• `Optional` **keywords**: *string*[]

**`description`** The default keywords used for SEO purposes.

Defined in: [types.d.ts:93](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L93)

___

### knownIssuesUrl

• `Optional` **knownIssuesUrl**: *string* \| URL

**`description`** Link for the error page to show known issues list.

Defined in: [types.d.ts:421](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L421)

___

### manifest

• `Optional` **manifest**: *any*

Defined in: [types.d.ts:465](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L465)

___

### noSSR

• `Optional` **noSSR**: *boolean*

**`description`** flag to turn off server-side-rendering. This is not typically beneficial.

**`example`** <caption>Turn off SSR</caption>
```json
"noSSR": true
```

Defined in: [types.d.ts:37](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L37)

___

### outputClasses

• `Optional` **outputClasses**: *any*

Defined in: [types.d.ts:466](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L466)

___

### permalinkFormat

• `Optional` **permalinkFormat**: *string*

**`description`** permalink format string.

**`default`** null

**`param`** window.location object.

**`param`** the current content object. see /api/content/content-path.

**`example:`** 
```json
  permalinkFormat: "${location.origin}/my/silly/path/${content.id}"
```

Defined in: [types.d.ts:477](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L477)

___

### prerenderToc

• `Optional` **prerenderToc**: *boolean*

**`description`** By default, we render the left-side "Table of Contents" for the site section server-side.
If you are dealing with a rather large sitemap, this can cause response times to be slow.
setting this value to false causes the ToC to render after the page has been loaded, allowing the page
to load faster.

**`default`** true

**`example`** 
```json
"prerenderToc": false
```

Defined in: [types.d.ts:141](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L141)

___

### prettifyCode

• `Optional` **prettifyCode**: *boolean*

**`description`** Prettify Option to prettify code blocks.

**`deprecated`** 

Defined in: [types.d.ts:378](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L378)

___

### prettifyCodeLang

• `Optional` **prettifyCodeLang**: *string*

**`description`** Prettify Option for highlight.js to set the language to use for syntax highlighting.

**`deprecated`** 

Defined in: [types.d.ts:388](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L388)

___

### prettifyCopyBadge

• `Optional` **prettifyCopyBadge**: *boolean*

**`description`** Prettify Option adding a copy-paste icon to the code blocks.

**`deprecated`** 

Defined in: [types.d.ts:417](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L417)

___

### prettifyGlobalLineNumbers

• `Optional` **prettifyGlobalLineNumbers**: *boolean*

**`description`** Prettify Option for highlight.js to turn on line numbers for every code block.

**`default`** false

**`deprecated`** 

Defined in: [types.d.ts:407](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L407)

___

### prettifyLineNumberDecorator

• `Optional` **prettifyLineNumberDecorator**: *string*

**`description`** Prettify Option for highlight.js to set the line number decoration typically ":", ")", or ".".

**`deprecated`** 

Defined in: [types.d.ts:412](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L412)

___

### prettifyPre

• `Optional` **prettifyPre**: *boolean*

**`description`** Prettify Option to prettify pre elements within code blocks.

**`deprecated`** 

Defined in: [types.d.ts:383](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L383)

___

### prettifySelector

• `Optional` **prettifySelector**: *string*

**`description`** Prettify Option for highlight.js to set the CSS selectors to convert for syntax highlighting.

**`default`** 'pre code, pre.codeblock'

**`deprecated`** 

Defined in: [types.d.ts:401](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L401)

___

### prettifyTheme

• `Optional` **prettifyTheme**: *string*

**`description`** Prettify Option for highlight.js to set the theme to use for syntax highlighting.
May use any listed here https://github.com/highlightjs/highlight.js/tree/main/src/styles

**`default`** 'googlecode'

**`deprecated`** 

Defined in: [types.d.ts:395](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L395)

___

### redirects

• `Optional` **redirects**: [*IRedirects*](iredirects.md)

**`description`** Redirects for requested URLs and query parameters.

Defined in: [types.d.ts:439](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L439)

___

### relatedResources

• `Optional` **relatedResources**: [*IPortalLinksEntity*](iportallinksentity.md)[]

**`description`** additional links to for related navigtation items. Overridden by easyDita's relatedResources feature.

**`deprecated`** 

Defined in: [types.d.ts:373](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L373)

___

### scripts

• `Optional` **scripts**: *string*[]

**`description`** custom JavaScript files to include as part of the page load.

**`example`** 
```json
"stripts": ["https://my.favorite.cdn/sompe-fancy-javscript.js"]
```

Defined in: [types.d.ts:360](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L360)

___

### search

• `Optional` **search**: *any*

**`description`** Content portal search configuration
{@link IPortalSearchOpts

Defined in: [types.d.ts:191](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L191)

___

### sectionFilter

• `Optional` **sectionFilter**: [*IPortalSectionFilter*](iportalsectionfilter.md)

**`description`** By default, we only show sitesections configured in the sitemap as the top level navigation.
You can, however, choose to change this to match on any of the siteSection attributes.
This will typically not need adjusted unless you are linking toa root map that isn't a sitemap.

**`default`** {"type": "sitesection"},

**`example`** <caption>Match any dita elements at the top level of the map</caption>
```json
"sectionFilter": {"type": ".*"}
```

**`example`** <caption>Match sitedections and topicheads at the top level of the map</caption>
```json
"sectionFilter": {"type": "(sitesection|topichead)"}
```

**`example`** <caption>Match everything except topicrefs at the top level of the map</caption>
```json
"sectionFilter": {"type": "!topicref"}
```

Defined in: [types.d.ts:129](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L129)

___

### seo

• `Optional` **seo**: [*IPortalSeo*](iportalseo.md)

**`description`** seo configuration flags.
[IPortalSeo](iportalseo.md)

Defined in: [types.d.ts:247](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L247)

___

### stylesheets

• `Optional` **stylesheets**: *string*[]

**`description`** custom CSS stylesheet files to include as part of the page load.

**`example`** 
```json
"stylesheets": ["https://my.favorite.cdn/custom-styling-items.css"]
```

Defined in: [types.d.ts:368](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L368)

___

### supportedBrowserMinimumVersions

• `Optional` **supportedBrowserMinimumVersions**: *any*

**`description`** The list of minimum required versions for supported browsers

**`example`** 
```json
"chrome": "78.0.3904.97",
"firefox": "73.0.1",
```

Defined in: [types.d.ts:230](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L230)

___

### tenant

• `Optional` **tenant**: *string*

**`description`** The name of the tenant for tracking purposes.

**`example`** <caption>The tenant name or org in easyDita</caption>
```json
"tenant": "jorsek-docs"
```

Defined in: [types.d.ts:45](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L45)

___

### theme

• `Optional` **theme**: *any*

**`description`** a Matrial-ui theme/jss object.
See https://material-ui.com/customization/theming/ and
https://github.com/Jorsek/content-portal-themes for more documentation

**`default`** {extends: "whitelabel"}

**`example`** <caption>a basic example:</caption>
```json
"theme":  {
   "palette": {
      "type": "light",
      "primary": {
          "dark": "#333",
          "main": "#666",
          "light": "#999",
          "contrastText": "#DDD"
      },
      "secondary": {
          "main": "rgb(20,120,155)",
      }
  }
},
```

Defined in: [types.d.ts:81](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L81)

___

### title

• `Optional` **title**: *string*

**`description`** The default HTML title for the site.

Defined in: [types.d.ts:85](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L85)

___

### toc

• `Optional` **toc**: [*IPortalToc*](iportaltoc.md)

**`description`** toc configuration options
[IPortalToc](iportaltoc.md)

Defined in: [types.d.ts:186](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L186)

___

### unsupportedBrowserFile

• `Optional` **unsupportedBrowserFile**: *string*

**`description`** The path of the file on the server to render when a browser is unsupported.

**`example`** <caption>Custom file as a *.{js/ts} file</caption>
```ts
export default (config: IUnsupportedBrowserConfig)=> `
<!DOCTYPE html>
<html>
  <head></head>
  <body>We are sorry, your browser may be out of date!</body>
</html>`
```

**`example`** <caption>simple custom html file</caption>
```html
<!DOCTYPE html>
<html>
  <head></head>
  <body>We are sorry, your browser may be out of date!</body>
</html>
```

Defined in: [types.d.ts:212](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L212)

___

### unsupportedBrowserRegExp

• `Optional` **unsupportedBrowserRegExp**: *string*

**`description`** a regular expression string to check against the user agent string to test if a browser is unsupported
see https://www.regextester.com/112058

**`example`** <caption>by default, we test if the user-agent is IE 10 or below.</caption>
```json
"unsupportedBrowserRegExp": "(opera|chrome|safari|firefox|msie|trident(?=\\/))\\/?\\s*(\\d+)"
```

Defined in: [types.d.ts:221](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L221)

___

### webFonts

• `Optional` **webFonts**: *object*

**`description`** webfontloader configuration options https://github.com/typekit/webfontloader.

**`default`** See Example

**`example:`** 
```json
{
  google: {
    families: ['Material Icons', 'Material Icons Sharp']
  },
  custom: {
    families: ['Social'],
    urls: ['https://assets.portal.easydita.com/fonts/social-icons.css']
  }
}
```

#### Type declaration:

Defined in: [types.d.ts:464](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L464)
