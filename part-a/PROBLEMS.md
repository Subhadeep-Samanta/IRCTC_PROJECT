# IRCTC Problem Discovery — Part A

## Summary

* Total problems documented: 6 (3 given + 3 self-discovered)
* Platform explored: irctc.co.in
* Devices used: Desktop Chrome and Mobile Chrome

---

## Problem 1: Tatkal Booking Crashes at 10:00 AM [Given]

### What is broken

During Tatkal opening hours, the booking flow becomes extremely slow or unresponsive. Users receive little feedback about their position in the system and often lose booking opportunities.

### Affected users

* Emergency travelers
* Working professionals
* Students
* Daily passengers

### Frequency

Daily at Tatkal opening times.

### Current Flow

1. User opens IRCTC at 9:50 AM.
2. User logs in.
3. User searches for train.
4. User selects Tatkal quota.
5. User fills passenger details.
6. User waits for booking window.
7. User clicks Book Now.
8. Website slows down or becomes unresponsive.
9. User refreshes repeatedly.
10. Tatkal quota gets exhausted.

### Where exactly it breaks

Step 7–8. Heavy traffic causes delays and insufficient feedback is provided.

---

## Problem 2: Search Filters Do Not Work Reliably [Given]

### What is broken

Filters such as class, departure time, and availability may not persist when navigating between pages.

### Affected users

* First-time users
* Mobile users
* Travelers comparing trains

### Frequency

Frequently during train searches.

### Current Flow

1. User searches trains.
2. Search results appear.
3. User applies Sleeper filter.
4. User applies Available Seats filter.
5. User applies Departure Time filter.
6. User opens a train result.
7. User returns to results page.
8. Filters reset or behave inconsistently.

### Where exactly it breaks

Step 7–8. Filter state is not consistently maintained.

---

## Problem 3: Seat Selection Resets [Given]

### What is broken

Selected berth preferences may not persist through the booking process.

### Affected users

* Senior citizens
* Families
* Passengers requiring lower berths

### Frequency

Intermittent but noticeable.

### Current Flow

1. User searches train.
2. User selects class.
3. User enters passenger details.
4. User chooses Lower Berth.
5. User proceeds.
6. Review page loads.
7. Preference is missing or changed.

### Where exactly it breaks

Step 5–6. User preference is not reliably carried forward.

---

## Problem 4: PNR Status Feature Is Difficult To Discover [Self-Discovered]

### How I found it

While trying to locate ticket status information from the homepage.

### What is broken

PNR status functionality is not immediately visible to users.

### Affected users

* First-time travelers
* Elderly users
* Occasional passengers

### Frequency

Every time users need ticket status.

### Current Flow

1. User opens homepage.
2. User searches for PNR status.
3. User navigates menus.
4. User locates enquiry section.
5. User enters PNR number.
6. Status is displayed.

### Where exactly it breaks

Step 2–4. Feature discoverability is poor.

### Screenshot / Description

Attach screenshot in assets/screenshots.

---

## Problem 5: Mobile Booking Experience Requires Excessive Scrolling [Self-Discovered]

### How I found it

While testing train booking on a mobile browser.

### What is broken

Several booking screens require excessive scrolling and form interaction.

### Affected users

* Mobile users
* Elderly users

### Frequency

Every mobile booking session.

### Current Flow

1. User opens mobile site.
2. User searches trains.
3. User selects train.
4. Passenger form loads.
5. User scrolls through multiple sections.
6. User reviews booking information.
7. User proceeds.

### Where exactly it breaks

Step 4–6. Long forms increase friction.

### Screenshot / Description

Attach screenshot in assets/screenshots.

---

## Problem 6: Refund Information Is Not Prominent During Cancellation [Self-Discovered]

### How I found it

While exploring ticket cancellation workflow.

### What is broken

Refund amount and deductions are not prominently displayed before cancellation.

### Affected users

* General passengers
* New users

### Frequency

Every cancellation attempt.

### Current Flow

1. User opens booking history.
2. User selects ticket.
3. User chooses Cancel Ticket.
4. Cancellation page loads.
5. User looks for refund estimate.
6. Information is difficult to find.
7. User proceeds with uncertainty.

### Where exactly it breaks

Step 5–6. Critical refund information lacks visibility.

### Screenshot / Description

Attach screenshot in assets/screenshots.
