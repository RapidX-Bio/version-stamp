# version-stamp

`latest.json` names the newest release of the RapidX qPCR unit software:

```json
{"version":"0.<rev>.0"}
```

The unit's web UI reads it from
`https://raw.githubusercontent.com/RapidX-Bio/version-stamp/main/latest.json`
and shows an update banner when the unit runs an older version. It is public
because the web UI reads it with no credentials; it carries nothing but the
version number.

CI writes it after every release (the `latest` job in the suite's
`release.yml`, through a write-enabled deploy key). Do not edit it by hand.
