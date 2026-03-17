# Privacy Policy

**EmergencyApp by NexGenHealth**
*Last updated: March 16, 2026*

## Introduction

NexGenHealth ("we", "our", "us") operates the EmergencyApp mobile application ("the App"). This privacy policy explains how we collect, use, and protect your personal information when you use our App.

Contact: NexGenHealth.io@gmail.com

## Information We Collect

### Information You Provide
- **Emergency Contacts**: Names, phone numbers, email addresses, and relationship labels of contacts you manually add to the App. This data is stored locally on your device in encrypted storage and is never transmitted to our servers.
- **Notification Preferences**: Your alert settings, delivery preferences, and configured notification groups. Stored locally on your device.

### Information Collected Automatically
- **GPS Location**: Your device's geographic coordinates are used to show your position on the map, calculate proximity to emergency events, generate egress routes, and include your location in emergency SMS messages you choose to send. Location data is processed locally on your device.
- **Plus Codes**: An encoded form of your GPS coordinates (Open Location Code) generated locally on your device for use in emergency messages.

### Information We Do NOT Collect
- We do not collect, store, or transmit your personal data to any server owned or operated by NexGenHealth.
- We do not track your location history on any external server.
- We do not sell, share, or monetize any personal information.
- We do not use analytics, advertising, or tracking SDKs.

## How We Use Your Information

| Data | Purpose | Stored Where | Encrypted |
|------|---------|-------------|-----------|
| GPS Location | Map display, proximity alerts, egress routing, emergency SMS | Device only (RAM + temporary cache) | Cache encrypted, auto-deleted after 24 hours |
| Emergency Contacts | SMS emergency alerts when you initiate them | Device only (AsyncStorage) | Yes — encrypted with device keystore |
| Notification Preferences | Filter which alerts you receive | Device only (AsyncStorage) | No (non-personal configuration data) |
| Message Queue | Offline SMS queuing for later delivery | Device only (AsyncStorage) | Yes — encrypted with device keystore |

## Third-Party Services

The App communicates with the following public government and scientific APIs to provide emergency data. These services receive your approximate GPS coordinates solely for the purpose of returning location-relevant alerts:

- **National Weather Service (NWS)** — weather alerts (api.weather.gov)
- **USGS** — earthquake data (earthquake.usgs.gov)
- **FEMA** — disaster declarations and IPAWS alerts (fema.gov)
- **NASA FIRMS** — wildfire/thermal hotspot data (firms.modaps.eosdis.nasa.gov)
- **NASA DONKI** — space weather data (api.nasa.gov)
- **NOAA SWPC** — space weather scales (services.swpc.noaa.gov)
- **EPA AirNow** — air quality data (airnowapi.org)
- **FDA** — food and drug recall data (api.fda.gov)
- **FBI** — most wanted data (api.fbi.gov)
- **DHS** — terrorism advisory data (dhs.gov)
- **OSRM** — route calculation for egress planning (router.project-osrm.org)
- **US State Department** — travel advisory data (travel.state.gov)
- **US Military COCOM** — combatant command news feeds (centcom.mil, africom.mil, etc.)

These services are operated by the United States government and NASA. Their respective privacy policies apply to data they process. We do not control these services.

### Payment Processing
If you choose to make a voluntary donation, you will be directed to Stripe's hosted payment page. No payment information is collected, processed, or stored by the App. Stripe's privacy policy governs payment data: https://stripe.com/privacy

### Map Tiles
Map tiles are loaded from OpenFreeMap (tiles.openfreemap.org) and other open tile providers. These services may log IP addresses per their standard server operations.

## SMS Messages

When you initiate an emergency alert or egress route notification, the App composes an SMS message containing:
- Your GPS coordinates
- Your Plus Code
- A Google Maps link to your location
- Active emergency alerts in your area (if any)
- Egress route waypoints and estimated times (if using the egress feature)

These messages are sent to contacts **you have selected** using your device's native SMS capability. The App does not send any SMS without your explicit action, except for optional periodic location updates which you must explicitly enable and configure.

## Silent Location Updates

If you enable the "Share Live Location" feature after sending an emergency or egress alert, the App will send periodic SMS messages with your updated GPS coordinates to the contacts you selected. This feature:
- Requires your explicit opt-in each time
- Has configurable intervals (5, 10, or 15 minutes)
- Has a configurable duration (30 or 60 minutes)
- Stops automatically after the configured duration
- Can be stopped at any time by closing the App

## Data Security

- **Encryption at rest**: Emergency contacts, message queue, and notification groups are encrypted using a key stored in the Android Keystore (hardware-backed secure enclave).
- **Encryption in transit**: All API communications use HTTPS (TLS). Cleartext HTTP traffic is blocked by the App's network security configuration.
- **No cloud storage**: All personal data remains on your device. There is no cloud backup or server-side storage of your data.
- **Auto-cleanup**: Cached GPS coordinates are automatically purged after 24 hours. Notification location data is scrubbed after 24 hours.

## Data Retention

- **Emergency Contacts**: Stored until you delete them manually.
- **Notifications**: Retained for up to 7 days, then automatically deleted.
- **Location Cache**: Automatically purged after 24 hours.
- **Message Queue**: Cleared after messages are sent successfully.
- **All Data**: You can delete all data at any time via Settings > Clear All Data.

## Permissions

The App requests the following Android permissions:

| Permission | Purpose |
|-----------|---------|
| ACCESS_FINE_LOCATION | GPS coordinates for emergency location and map |
| ACCESS_COARSE_LOCATION | Approximate location fallback |
| READ_CONTACTS | Pick emergency contacts from your address book |
| SEND_SMS | Send emergency alert and egress route messages |
| POST_NOTIFICATIONS | Display emergency alert notifications |
| VIBRATE | Haptic feedback for emergency notifications |
| INTERNET | Fetch emergency data from public APIs |
| RECEIVE_BOOT_COMPLETED | Restart background alert monitoring after device reboot |
| WAKE_LOCK | Keep alert monitoring active in background |

All permissions are used solely for the stated emergency safety purposes.

## Children's Privacy

This App is not directed at children under 13. We do not knowingly collect personal information from children.

## Changes to This Policy

We may update this privacy policy from time to time. Changes will be reflected in the "Last updated" date at the top of this document. Continued use of the App after changes constitutes acceptance.

## Contact Us

If you have questions about this privacy policy or your data:

**NexGenHealth**
Email: NexGenHealth.io@gmail.com

## Your Rights

You have the right to:
- Access all data stored by the App (visible in the App's Settings and Contacts screens)
- Delete all personal data at any time (Settings > Clear All Data)
- Disable any notification source or alert type
- Revoke location, contacts, or SMS permissions at any time via Android Settings
