# SR Holiday Tracker

Staff holiday booking and approval for **SR Electrical & Security**
(Stewart Rawson Electrical Ltd).

Holiday year runs 1 April – 31 March. England & Wales bank holidays are
calculated automatically for any year and never come out of anyone's allowance.

## Use it

Open the link on your phone, tablet or computer. On a phone:
**Share → Add to Home Screen** to run it full screen.

## What it does

- Personal dashboard — days taken, days left, carry-over, bonus days
- Request time off; the admin approves or rejects
- Team calendar colour-coded per person, with seasonal events and birthdays
- Holiday, sickness and other leave — only holiday uses the allowance
- Bulk-book the whole team for a Christmas shutdown
- Add and remove staff, set allowances, grant extra days
- Export to CSV

## Syncs across every device

Bookings are held in a Firebase Realtime Database and sync live between phones,
tablets, Macs and PCs. Book on one, it appears on the others within seconds —
no refresh needed.

Works with no signal too: changes are saved on the device and sent up
automatically once you're back online. The chip in the top bar shows
**Synced** or **Offline** so you always know where you stand.

## For integrations

Data lives under `/sr-holiday/v1` in the Realtime Database:

    /sr-holiday/v1/staff/{id}      name, allowance, bonus, carry-over, colour
    /sr-holiday/v1/bookings/{id}   staff, type (vac|sick|other), dates[], status, note

Anything that speaks HTTP can read and write it, which is how the Buzz agent
adds and removes holidays without anyone logging in.
