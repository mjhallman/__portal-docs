[@jorsek/content-portal-configs](../README.md) / [Exports](../modules.md) / I18nString

# Interface: I18nString

**`description`** a string key that maps to an i18n language file entry.
If the string ID is not defined in the i18n file,
the string returned is an HTML encoded value of the key.
see https://github.com/orneryd/web-components#I18n for more details.

**`example`** <caption>Given the language definition file</caption>
```json
i18n: {
  "en-US": {
    "label.tenant": "Jorsek"
  }
}
```

**`example`** <caption>The string "label.tenant" will be translated in the UI</caption>
```html
<i18n-message id="message.label">Jorsek</i18n-message>
```

**`example`** <caption>The string "label.something-else" will be translated in the UI as</caption>
```html
<i18n-message id="label.something-else">label.something-else</i18n-message>
```

**`example`** <caption>The string "I don't need a translation!" will be translated in the UI as</caption>
```html
<i18n-message id="label.something-else">You should definitely use translations anyway.</i18n-message>
```

## Hierarchy

* *any*

  ↳ **I18nString**
