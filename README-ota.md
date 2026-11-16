# OTA link for the friend

Page: https://jarnaljitsingh.com/star-gl-ota/   (Safari on the iPhone → tap "① Install the game")
Files here are published from this folder: repo `jarnaljitsingh/star-gl-ota`, IPA is a GitHub release asset (tag v1).

* IPA: `star-gl-share.ipa` — re-signed copy of the working build, profile `prof_2devices.mobileprovision`
  (devices: 00008110-000908413481401E = mine, 00008140-001A51D93444801C = friend). Expires 2027-06-09.
* To rebuild after any change: re-sign `../BACKUP-2026-11-16/PUBGM-FLASH-work.app` with that profile, zip to
  `Payload/ShadowTrackerExtra.app`, then `gh release upload v1 star-gl-share.ipa --clobber`.
* Friend's steps: install → open → the app asks for the data file → he downloads it from the link on the page
  (Safari keeps it in Downloads) → app imports it → enter his key.
* If iOS shows "Untrusted Developer": Settings → General → VPN & Device Management → trust the cert.
* Note: 1 key = 1 device. Whichever phone logs in last re-registers itself on the panel; if mine stops working
  after he logs in, that's why (fix = log in again on mine, or load the spoof dylib).
