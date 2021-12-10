[@jorsek/content-portal-configs](../README.md) / [Exports](../modules.md) / ILunrSearchOpts

# Interface: ILunrSearchOpts

## Hierarchy

* **ILunrSearchOpts**

  ↳ [*IPortalSearchOpts*](iportalsearchopts.md)

## Table of contents

### Properties

- [fields](ilunrsearchopts.md#fields)
- [ref](ilunrsearchopts.md#ref)

## Properties

### fields

• `Optional` **fields**: *string*[]

**`description`** the fields for Lunr to index for content objects (when using a bundle only)

**`default`** ["href","shortDescription","title"]

Defined in: [types.d.ts:395](https://github.com/Jorsek/content-portal-config/blob/a084865/types.d.ts#L395)

___

### ref

• `Optional` **ref**: *string*

**`description`** the ref to use at the key for Lunr search (when using a bundle only)

**`default`** "href"

Defined in: [types.d.ts:390](https://github.com/Jorsek/content-portal-config/blob/a084865/types.d.ts#L390)
