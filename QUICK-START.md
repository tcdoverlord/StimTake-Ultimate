# StimTake Ultimate — Quick Start (2.7.3)

## Install

Download `StimTakeStudio-Setup-2.7.3.exe` from the official Releases page. Close StimTake before upgrading; export a full workspace backup and Viewer Intelligence JSON pack first. The installed product is named StimTake Studio. A fresh setup starts with an empty workspace and overlay slots.

## Connect OBS

1. Start StimTake Studio and import an overlay into a slot.
2. In OBS, add a Browser Source and enter `http://127.0.0.1:8790/obs.html`.
3. Set the source dimensions to suit your overlay canvas (for example, 1920 × 1080).
4. Activate an overlay from StimTake and verify that it appears in OBS.

Keep StimTake running. Its local service is intended for loopback access; do not expose its port to the internet.

## Connect Chaturbate

1. Open the Chaturbate Bridge in StimTake.
2. Open Chaturbate Token Settings and authorize a private Events API token.
3. Copy your own complete Events API URL into StimTake and select **Test Connection & Connect**.
4. Verify that live events appear in the Bridge. Do not run a second poller against the same feed.

The Events API URL is a private credential, different from your OBS stream key. The native bridge stores it using Windows DPAPI for the current Windows user. Never publish the URL, unredacted logs, or private viewer records.

## Viewer Intelligence and arrivals

- Save a viewer profile with a welcome draft, interests, notes or reminders.
- Open Arrivals and select **Personalized profiles / VIPs**, **All named viewers**, or **Off**.
- Notifications appear for matching new named entry events received after the watcher is ready. Copy Welcome copies a draft; StimTake does not automatically send it. Dismiss advances through the pending queue.
- The queue holds up to 50 entries. The watcher polls the latest 100 events and may miss events under very high traffic or interruptions.
- Viewer Intelligence shows live totals, filters, sorting, and selection across pages. Categories can overlap. Bulk deletion prompts for confirmation; protected profiles require an additional confirmation.
- Automatic viewer saving defaults to on. Turn it off to stop creating new basic viewer records; existing saved profiles continue tracking activity, and arrival notifications remain independent. Deleted profiles can reappear if automatic saving is on.

For support, use [GitHub Issues](https://github.com/tcdoverlord/StimTake-Ultimate/issues) without revealing private data.
