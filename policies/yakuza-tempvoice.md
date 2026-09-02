# Privacy Policy — Yakuza TempVoice

**Effective date:** September 3, 2026  
**Operator and deletion contact:** Yakuza Community — **yakuza.community@proton.me**

Yakuza TempVoice is a Discord application that creates and manages temporary voice rooms in approved Yakuza Community servers.

## Data we process

To operate temporary voice rooms, we process Discord server, channel, role, and user identifiers; member usernames used to generate a room name; voice-state events indicating that a member joined, left, or moved voice channels; and member role membership needed to apply configured room controls and access rules.

When a temporary room is created or controlled, the application stores the room ID, server ID, owner ID, configured creator-channel ID, timestamps, room name, privacy mode, user limit, bitrate, region, status, chat setting, waiting-room setting, and the IDs of trusted, blocked, permitted, or transferred users. It also stores server and interface configuration, including configured channel, category, role, and message IDs.

The application writes operational audit records containing applicable server, room, actor, and target IDs, action type, timestamp, and relevant before/after configuration values. If a room owner enables a room password, the application stores only a salted SHA-256 hash and salt; it does not store the plaintext password.

## Why we process it

We use this data solely to create a temporary room when a member joins a configured creator channel; move the owner into that room; apply its access controls; provide owner and administrator controls such as rename, limit, privacy, invite, trust, block, waiting room, ownership transfer, and deletion; recover saved room preferences; synchronize existing rooms; and delete empty temporary rooms.

The application may temporarily retrieve avatars of members currently present in active temporary voice rooms to render an activity image in the Discord room-control interface. Avatar image buffers are used only for that rendering and are not stored in the application's database.

## What we do not process

Yakuza TempVoice does not request or read Message Content Intent. It does not read ordinary Discord messages, direct messages, message attachments, or message history for its service. It does not request or process Presence Intent, and does not collect presence or activity history. It does not sell data, use it for advertising, create behavioural profiles, or train AI or machine-learning models.

## Storage, retention, and sharing

The application stores its configuration, active-room, saved owner-setting, and audit data in its configured MongoDB database. Redis may hold short-lived locks and runtime cooldown state. Data is retained while needed for room management, saved owner preferences, operational recovery, security, or server administration; the application does not enforce a universal automatic 30-day deletion period.

The application uses Discord to provide its features and retrieves Discord-hosted avatar images only as described above. It does not disclose or sell personal data to advertisers or data brokers.

## Deletion requests

Users and server administrators may request deletion of applicable data by emailing **yakuza.community@proton.me**. Please include the relevant Discord user ID and, where available, server ID or temporary-room ID so we can locate the applicable records. Deleting a room with the option to wipe saved settings deletes that owner's saved room settings; applicable records may still be retained where necessary for security, administration, or legal obligations.

## Security and changes

The application restricts operation to configured approved servers, uses Discord permission overwrites for room access, and stores room passwords only as salted hashes. Storage-at-rest encryption depends on the configured database and hosting environment and is not represented by this policy as guaranteed by the application code alone.

We may update this policy when the service changes. The current version remains available at this URL.
