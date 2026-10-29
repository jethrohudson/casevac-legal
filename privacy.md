# CASEVAC Privacy Policy

**Effective date:** October 29, 2026

CASEVAC: Nearest Trauma Center ("CASEVAC" or "the app") is made by Mark Iglar, an individual developer ("I", "me"). This policy explains what the app does with your information. It is written to match what the app's code actually does.

**The short version:** CASEVAC has no account, no analytics, no advertising and no tracking, and I run no server that receives your data. Your notes, photos and principal profiles stay encrypted on your iPhone. Your location goes only to the services that need it to give you an answer (Apple Maps, Apple Weather, aviationweather.gov, and, if you turn it on, OpenStreetMap), and to your own team through iCloud when you choose to go On duty.

## 1. What I collect

**Nothing reaches me.** The app does not send any personal information, usage data, crash logs or identifiers to me or to any server I operate. There are no third-party analytics, advertising or tracking libraries in the app.

If you choose to share crash reports with app developers in your iPhone settings (Settings › Privacy & Security › Analytics & Improvements), Apple may give me anonymous crash reports. That is controlled by Apple and by you, not by the app.

## 2. Your location

The app uses your location to find the nearest emergency rooms and trauma centers, build driving routes, find landing zones and show the weather.

- **When:** only while the app is open ("While Using"). The one exception is Team sharing (section 4). If you go On duty *and* turn on background sharing, the app asks for "Always" permission so your team can still see you while the app isn't on screen. Sharing stops when you go off duty or your shift ends.
- **On your iPhone:** your last results (nearest hospitals and the spot they were calculated from), cached weather and cached landing-zone results are kept in the app's storage on your iPhone, protected by iOS Data Protection.
- **Where it goes:**
    - **Apple Maps (MapKit):** your current location and the destination are sent to Apple to calculate drive times and routes, and the map itself comes from Apple. Place searches you type in the advance tools also go to Apple. Apple's Privacy Policy applies: <https://www.apple.com/legal/privacy/>.
    - **Apple Weather (WeatherKit):** your location is sent to Apple to get current conditions for the map's weather chip.
    - **aviationweather.gov (U.S. National Weather Service / NOAA):** a search box around your approximate location (about 100 m precision) is sent to find the nearest airport weather report (METAR). The same is done for a landing zone or hospital helipad when you open flight weather.
    - **OpenStreetMap Overpass servers (only if Pro "candidate LZs" is on):** the search center, rounded to about 100 m, and the search radius are sent to public Overpass servers (overpass-api.de and community mirrors) to find open areas that might work as helicopter landing zones. You can turn this off in Settings.
    - **Navigation apps:** when you tap GO, the destination is handed to Apple Maps, Google Maps or Waze, whichever you choose. That app's own privacy policy then applies.
    - **Things you choose to share:** Share ETA, Copy location, Share LZ and similar buttons put your coordinates into a message only when you tap them. You pick who receives it.

These services see your request and your device's internet (IP) address, as any web service does. I do not receive any of it.

## 3. Field notes, team LZs, saved advance packs and photos

Hospital field notes (such as ER phone numbers, drop-off pins and entry notes), team landing zones, saved advance packs, and the photos you attach:

- are stored **only on your iPhone**, encrypted with AES-256 using a key kept in the iPhone Keychain ("this device only"), on top of iOS Data Protection;
- are **excluded from iCloud and computer backups**, so they are not restored to a new phone (export them if you want a copy);
- are **never uploaded** by the app. They leave your phone only if you use **Export notes** (Pro), which creates a JSON file that you save or send yourself. **That file is not encrypted.** Keep it safe and share it only with your team.

Photos come from your camera or photo library only when you tap **Camera** or **Library**. They are downscaled and encrypted. The app does not read the rest of your photo library.

## 4. Team location sharing (Pro, uses iCloud)

If you create or join a Team, the app uses **Apple's iCloud (CloudKit)** to share information within that team. The team lives in the iCloud account of the person who created it. Only people that person invites through Apple's sharing can see it. I cannot see it.

What is shared with your team:

- **Your profile:** callsign, name, role, phone number and map color. These are stored in your team's iCloud records.
- **Status:** On duty or off duty, SOS alerts, battery level (you can turn this off) and the time of your last update.
- **While you are On duty only:** your coordinates, heading and speed. These are stored in CloudKit **end-to-end encrypted fields**, which Apple says even Apple cannot read. Your coordinates are removed from the shared record when you go off duty. On duty turns itself off when your shift length ends.
- **Rally point:** a name and location set by a team member, also end-to-end encrypted.

**Leaving a team** deletes your member record. If you created the team, leaving deletes the whole team for everyone. Team alerts use Apple Push Notifications.

Your team profile is also kept on your iPhone in the app's settings.

## 5. Principal medical profiles

Medical profiles you enter for the people you protect (such as allergies, medications, blood type, conditions, physicians and emergency contacts):

- are stored **only on your iPhone**, in their own encrypted file (AES-256-GCM) with a separate key that requires a device passcode and never leaves the device;
- open only with Face ID or your passcode, and lock automatically when you leave those screens or the app;
- are **never synced, never sent to iCloud or your team, never included in Export notes, and excluded from backups**.

If you create the **ER handoff PDF**, it is made on your iPhone and is deleted from the iPhone when you close the preview. If you share or print it, you decide who receives it. The app reminds you to share it only with treating clinicians. You are responsible for having the principal's permission to record and share their medical information.

## 6. Hospital and heliport data updates

The app ships with public hospital, trauma-center and heliport data. Once a day at most, it may download updated public data files from a GitHub Pages website (operated by GitHub, Inc.). **These requests contain no location or personal information.** Only standard internet information, such as your IP address, is seen by GitHub. See GitHub's Privacy Statement: <https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement>.

## 7. Purchases

CASEVAC Pro subscriptions are sold and processed by **Apple** through your Apple ID. I never see your name, payment card or Apple ID. The app only checks with Apple, on your device, whether you have an active subscription.

## 8. Permissions the app asks for

| Permission | Why | Required? |
|---|---|---|
| Location (While Using) | Nearest ER, routes, LZs, weather | Strongly recommended; GO and Call 911 work without it |
| Location (Always) | Team background sharing while On duty | Optional |
| Notifications | Team SOS alerts and shift-end reminders | Optional |
| Face ID | Unlock principal medical profiles | Optional (passcode works too) |
| Camera / Photos | Attach photos to field notes and LZs | Optional |

You can change these at any time in iPhone Settings › CASEVAC.

## 9. Apple's privacy manifest

The app's privacy manifest (PrivacyInfo.xcprivacy) says the app does **no tracking** and lists no tracking domains. It declares only **approximate location**, used for app functionality and not linked to your identity. It also declares the app's use of iOS "UserDefaults" to store its own settings.

## 10. How long data is kept, and how to delete it

- **On your iPhone:** until you delete it in the app or delete the app. Deleting the app removes the app's on-device data. Encryption keys stored in the Keychain may remain until the device is erased, but without the data they protect nothing.
- **Team data in iCloud:** your location is cleared when you go off duty. Your member record is deleted when you leave the team, and the whole team is deleted when its creator leaves.
- **Third-party services** (Apple, NOAA/aviationweather.gov, OpenStreetMap servers, GitHub) keep request information under their own policies.

Because I hold no data about you, there is nothing for me to access, correct or delete on my side. You control all app data on your device. If you have a question or a privacy request, contact me (section 13).

## 11. Children

CASEVAC is a professional tool for executive-protection and security teams. It is not directed to children under 13, and I do not knowingly collect information from children.

## 12. Changes

If this policy changes, I will update the date at the top and post the new version at this address. Important changes will also be noted in the app's release notes.

## 13. Contact

Mark Iglar, developer of CASEVAC  
Email: **[iglarm@me.com](mailto:iglarm@me.com)**
