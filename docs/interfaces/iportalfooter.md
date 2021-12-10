[@jorsek/content-portal-configs](../README.md) / [Exports](../modules.md) / IPortalFooter

# Interface: IPortalFooter

## Table of contents

### Properties

- [copyright](iportalfooter.md#copyright)
- [links](iportalfooter.md#links)
- [linksHeader](iportalfooter.md#linksheader)
- [logoAlt](iportalfooter.md#logoalt)
- [logoSrc](iportalfooter.md#logosrc)

## Properties

### copyright

• `Optional` **copyright**: [*I18nString*](i18nstring.md)

**`description`** the copyright string to use for the footer.

**`default`** "message.footer.copyright"

Defined in: [types.d.ts:817](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L817)

___

### links

• `Optional` **links**: [*IPortalLinksEntity*](iportallinksentity.md)[]

**`description`** the links to be placedin the footer.

**`example`** 
```json
"footer": {
"logoSrc": "https://assets.portal.easydita.com/media/jorsek-logo.png",
"logoAlt": "Jorsek",
"links": [
{
"target": "_blank",
"href": "https://easydita.com/",
"text": "Homepage"
},
{
"href": "https://easydita.com/legal",
"text": "Legal"
},
{
"href": "https://easydita.com/about",
"text": "About Us"
},
{
"href": "https://easydita.com/privacy-notice",
"text": "Privacy Notice"
},
{
"href": "https://easydita.com/contact-us",
"text": "Contact Us"
},
{
"href": "https://easydita.com/terms-of-use",
"text": "Website Terms of Use"
}
]
},
```

Defined in: [types.d.ts:855](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L855)

___

### linksHeader

• `Optional` **linksHeader**: [*I18nString*](i18nstring.md)

**`description`** the string to use for the footer header.

Defined in: [types.d.ts:807](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L807)

___

### logoAlt

• `Optional` **logoAlt**: *string*

Defined in: [types.d.ts:812](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L812)

___

### logoSrc

• `Optional` **logoSrc**: *string*

**`description`** the image url to use for the footer logo.

Defined in: [types.d.ts:811](https://github.com/Jorsek/content-portal-config/blob/f120983/types.d.ts#L811)
