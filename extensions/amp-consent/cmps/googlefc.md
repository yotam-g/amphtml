# GoogleFC

## Example

```html
<amp-consent id="consent" layout="nodisplay" type="googlefc">
  <script type="application/json">
    {
      "clientConfig": {
        "publisherIdentifier": "id"
      }
      "postPromptUI": "fcConsentRevocation",
      "uiConfig": {
        "overlay":true
      },
    }
  </script>

  <div id="fcConsentRevocation">
    <button on="tap:consent.prompt(consent=googlefc, expireCache=true)">
      Revoke my user consent.
    </button>
  </div>
</amp-consent>
```

## Configuration (`clientConfig`)

| Attribute |  Type  | Mandatory | Description                                                                                                                                                                                                |
| --------- | :----: | :-------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| publisherIdentifier    | String |    yes    | This is your publisher identifier that uniquely identifies your Google publisher account. It will be provided in the generated amp-consent extension.