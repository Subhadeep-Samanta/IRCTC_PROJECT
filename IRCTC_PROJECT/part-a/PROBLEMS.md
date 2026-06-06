# IRCTC Problem Discovery — Part A

## Summary

- Total problems documented: 6
- Platform explored: irctc.co.in
- Devices used: Desktop Chrome and Mobile Chrome

---

# Problem 1: Tatkal Booking Crashes at 10:00 AM [Given]

## What is broken

Users experience slow loading, timeouts, and booking failures during Tatkal booking hours due to extremely high traffic.

## Affected Users

Emergency travelers, working professionals, students, and daily passengers.

## Frequency

Daily during Tatkal opening hours.

## Current Flow

1. User opens IRCTC at 9:50 AM.
2. User logs into account.
3. User searches train.
4. User selects Tatkal quota.
5. User fills passenger details.
6. User waits for quota opening.
7. User clicks Book Now.
8. System becomes slow.
9. User refreshes multiple times.
10. Quota gets exhausted.

## Where Exactly It Breaks

Step 7–8 when thousands of users send booking requests simultaneously.

---

# Problem 2: Search Filters Do Not Work Reliably [Given]

## What is broken

Applied filters do not always persist and results may appear inconsistent.

## Affected Users

Passengers comparing trains and classes.

## Frequency

Frequently during train searches.

## Current Flow

1. User searches trains.
2. Search results appear.
3. User selects Sleeper Class.
4. User selects Available Seats Only.
5. User selects Morning Departure.
6. Results update.
7. User opens train details.
8. User returns.
9. Filters reset.

## Where Exactly It Breaks

Step 8–9 where filter state is lost.

---

# Problem 3: Seat Selection Resets [Given]

## What is broken

Selected berth preferences are not always retained.

## Affected Users

Senior citizens, families, and passengers requiring specific berths.

## Frequency

Occasional but noticeable.

## Current Flow

1. User searches train.
2. User selects class.
3. User enters passenger information.
4. User selects Lower Berth.
5. User proceeds.
6. Review page opens.
7. Preference disappears.

## Where Exactly It Breaks

Step 5–6 where selected preference is not retained.

---

# Problem 4: PNR Status Is Difficult To Discover [Self-Discovered]

## How I Found It

While attempting to locate PNR status from the homepage.

## What is broken

PNR status is not immediately visible and requires menu navigation.

## Affected Users

Occasional travelers and first-time users.

## Frequency

Every time a user checks ticket status.

## Current Flow

1. User opens homepage.
2. Searches for PNR option.
3. Scans menus.
4. Navigates to enquiry section.
5. Finds PNR status.
6. Enters PNR.
7. Gets result.

## Where Exactly It Breaks

Step 2–4 due to poor discoverability.

## Screenshot

assets/screenshots/pnr-status.png

---

# Problem 5: Mobile Website Requires Excessive Scrolling [Self-Discovered]

## How I Found It

While performing booking tasks on a mobile browser.

## What is broken

Booking forms are long and require excessive scrolling.

## Affected Users

Mobile users.

## Frequency

Every mobile booking session.

## Current Flow

1. User opens mobile website.
2. Searches train.
3. Selects train.
4. Passenger form loads.
5. User scrolls through multiple sections.
6. Reviews details.
7. Continues booking.

## Where Exactly It Breaks

Step 4–6 due to long forms and dense information.

## Screenshot

assets/screenshots/mobile-booking.png

---

# Problem 6: Refund Information Is Not Clearly Visible [Self-Discovered]

## How I Found It

While exploring ticket cancellation flow.

## What is broken

Refund amount and deductions are not clearly displayed.

## Affected Users

Passengers cancelling tickets.

## Frequency

Every cancellation attempt.

## Current Flow

1. User opens booked ticket history.
2. Selects ticket.
3. Clicks Cancel Ticket.
4. Cancellation page opens.
5. User looks for refund amount.
6. Information is difficult to locate.
7. User proceeds without clarity.

## Where Exactly It Breaks

Step 5–6 because refund details are not prominently displayed.

## Screenshot

assets/screenshots/refund-info.png