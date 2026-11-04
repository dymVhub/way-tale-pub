---
layout: page
title: Privacy policy
permalink: /en/privacy
lang: en
---

Effective: 31 October 2026. Русская версия: [Политика конфиденциальности](../privacy).

## Contact

comeahead.dev@gmail.com

## What the app does

Waytale records your location continuously in the background, also when the app is closed. From the recording it opens a "fog of war" map and draws your path by day. The recording is stored on your phone in a local database. Local data is not included in the phone's cloud backups (Android Auto Backup is off).

## Without sign-in

Without signing in, and with sync off, location data does not leave your phone (except map requests, see below). Sync is off by default on new installs.

## Sign-in and account

Sign-in is only with Google. From Google the app gets your name, email and profile photo URL. Friends never see your email or account id, only the name you chose.

## Sync

With sync on, your account on Supabase servers (Postgres) stores explored areas, the daily path, daily statistics and visited cities. If "Record the path you walked" is off, the path is not recorded at all, only explored areas. Only the account owner can access this data (row-level security).

## Friends and live location

- Friends are added only with an invitation code. There are no public profiles.
- A friend sees your path only for the days (or a part of a day) you explicitly shared. You can revoke sharing. If you delete a day's path, it is also removed for the friend.
- Live location goes only to the friends you choose, for the time you choose. The server keeps only the last point, no history; it is deleted when the time ends.

## Notifications

Push notifications use Firebase Cloud Messaging (Google). The device push token is stored on the server. A push contains only a friend's name and dates, no places.

## Analytics

We use Firebase Analytics (Google): which screens are opened and which actions are taken. Analytics gets no coordinates, path data, friends' names, email or account id. Detailed location and device data and Google signals are turned off. Data is kept for 2 months. The advertising ID is not collected. There are no ads.

## Crash reports

Sentry (EU region) receives error details, device model, OS version, language and time zone. Coordinates are filtered out, IP addresses are not stored, there are no screenshots.

## Map and cities

Map images are loaded from OpenFreeMap (based on OpenStreetMap). Like with any online map, the server sees which map area is requested and your IP address. City borders are downloaded from Cloudflare R2 storage as files for areas about 70 km across, without any identifiers.

## Import from Google Timeline

The file is processed only on the phone, never uploaded, and not kept after import.

## Permissions

- Location "while using" and "all the time": for background recording.
- Physical activity: to tell movement from rest and save battery.
- Notifications: the live location sharing notice and friends' pushes. Everything works without this permission.

## Selling data

We do not sell data and do not share it for advertising.

## How data is protected

- All data between the app and the servers (Supabase, Firebase, Sentry, map and city files) goes over an encrypted connection (HTTPS).
- On the server, the data of an account is available only to that account (row-level security). Friends get access only to what you explicitly shared with them.
- The sign-in session is kept in the phone's protected storage.
- Data on the phone lives in the app's private storage, other apps have no access to it.
- Coordinates are filtered out of crash reports and are never sent to analytics.

## How long data is kept

- On the phone: until you delete it (or remove the app).
- In the account on the server: until you delete it or delete the account. The line of a deleted day's path is erased from the server at once; only a mark that the day was deleted remains.
- Live location: only the last point, deleted when the chosen time ends.
- Push token: removed on sign-out and with the account.
- Analytics: 2 months.
- Crash reports: no longer than 90 days.
- After account deletion nothing is kept on purpose. Copies may remain in the server's backups for up to 7 days, then they disappear.

## Deleting data

How to delete your data and account: [deletion page](delete-account).

## Children

The app is not intended for children under 13. <!-- owner: confirm -->

## Changes

Changes to this policy are published on this page with a new date.
