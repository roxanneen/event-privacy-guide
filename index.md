## Protect Your Device at Industry Events 

**Attending or speaking at a large-scale conference or niche industry meetup?** Watch out for radio fingerprinting + ad-network matchmaking. Vendors promise sponsors and organizers that they can profile every device in the room and retarget you with unwanted ads—often for token pre‑sales, crypto pitches or remarketing campaigns you never opted into.


---

### TL;DR
A simple, effective guide to stop your device from becoming an ad‑unit: no illegal jammers, no arcane legal clauses—just smart privacy hygiene.

| Layer                 | Countermeasure                                 |
|:----------------------|:-----------------------------------------------|
| **MAC Randomization** | Enable on iOS (≥8) & Android (≥6) for Wi‑Fi & BLE probe requests.
| **Airplane Mode + Cell** | Use airplane mode, then selectively re-enable cellular if needed.
| **RF Shielding**      | Faraday pouch or RF‑blocking sleeve when idle.
| **App Permissions**    | Deny event‑app access to Bluetooth, Location, Nearby Devices.
| **Post‑Event Cleanup**| Forget networks & reset your Advertising ID.


---

### 1. How They Track You
1. **Probe‑Request Sniffing**  
   • Phones broadcast Wi‑Fi and BLE probe requests for known SSIDs or paired devices.  
   • Scanners (e.g. Raspberry Pi + Kismet) capture MAC addresses and one‑way hash them for privacy.

2. **Hash Matching to Ad IDs**  
   • Data Management Platforms ingest hashed MACs and match them against hashed Advertising IDs (IDFA/GAID) sourced from DSPs.  
   • A successful match lets advertisers retarget you across apps, networks or programmatic channels.

3. **Beacon SDKs**  
   • Event apps often embed BLE SDKs that emit/scan UUID beacons.  
   • Proximity data correlates your app’s UUID with registration info—fuel for granular profiling.


---

### 2. Defense Arsenal

<aside>**Note:** Radio jammers are illegal in most jurisdictions (including the UK and US) and can interfere with critical signals (medical devices, emergency beacons). Avoid them entirely.</aside>

| Layer                 | What to Do                                                                                                |
|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| **MAC Randomization** | ✔️ Enable in System Settings (iOS ≥8, Android ≥6) for Wi‑Fi & BLE.                                            |
| **Airplane Mode + Cell** | ✔️ Switch to airplane mode, then toggle cellular data back on for calls/SMS if required.                 |
| **RF Shielding**      | ✔️ Stow device in Faraday pouch or RF‑blocking sleeve when not actively in use.                              |
| **App Permissions**    | ✔️ Revoke Location, Bluetooth & Nearby‑device access in your event-app’s settings.                          |
| **VPN & DNS**         | ✔️ Use a VPN on venue Wi‑Fi and set private DNS (e.g. 1.1.1.1) to mask traffic, though it won’t hide probes. |
| **Post‑Event Cleanup**| ✔️ “Forget” venue SSIDs in Wi‑Fi settings and reset your Advertising ID (Settings → Privacy).               |


---

### 3. Best Practices for Organizers & Sponsors
- **Explicit Opt‑In**: Disclose any device‑profiling activities up front and obtain clear, granular consent—no buried clauses.
- **Privacy‑First App Builds**: Offer a "Lite" version of the event app without BLE or beacon SDKs.
- **Attendee Education**: Share this guide in pre‑event communications so participants can self‑protect.


---

### 4. Conclusion
Radio fingerprinting + ad‑network matchmaking may sound cutting‑edge, but it’s just wireless collisions and hash lookups. With MAC randomization, strategic airplane‑mode use, RF shielding and tightened app permissions, you can attend and speak with confidence—knowing your device isn’t fueling someone’s ad campaign behind the scenes.

