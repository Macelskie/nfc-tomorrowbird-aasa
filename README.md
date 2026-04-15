# nfc-tomorrowbird-aasa

Hosts the Apple App Site Association (AASA) file for `nfc.tomorrowbird.ai`.

Used by the MOCO NFC clock-in iOS app — the AASA file links the Universal Link domain to the app bundle ID `mv.MOCOWidget` with Team ID for automatic routing on tap.

## Structure

```
.well-known/apple-app-site-association   → required path, no .json suffix
CNAME                                    → nfc.tomorrowbird.ai
```

## Update Team ID

The `TEAMID_PLACEHOLDER` in `.well-known/apple-app-site-association` must be replaced with the 10-character Apple Team ID (from developer.apple.com/account).

## Verify

```bash
curl -I https://nfc.tomorrowbird.ai/.well-known/apple-app-site-association
curl https://app-site-association.cdn-apple.com/a/v1/nfc.tomorrowbird.ai
```
