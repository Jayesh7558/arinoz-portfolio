# Muddemaal Management System

Oct 1, 2026 · @Jayesh Nitin Talele

## Project Overview

The Muddemaal Management System is a digital platform that records, stores, tracks and disposes of case property seized by police, with a complete chain of custody for every item.

"Muddemaal" is the property police seize during an investigation: vehicles, cash, jewellery, weapons, drugs, mobile phones, documents and other evidence. It is kept in the police station's store room, called the malkhana, until the court decides what happens to it.

The system replaces handwritten malkhana registers with a searchable database. Every item gets a unique QR-coded tag, a fixed storage location and a full history of who handled it, when, and why.

**Who it is for**

- **Investigating Officer (IO)** — registers seized property against the FIR and requests its movement to court or the forensic lab.
- **Malkhana in-charge** — receives, stores, issues and takes back items, and keeps the inventory accurate.
- **Station House Officer (SHO)** — approves movements, returns and disposals, and reviews pending items.
- **Senior officers** — monitor property across stations through dashboards and audit reports.

**Key capabilities**

- Digital seizure entry linked to the FIR or case number
- QR / barcode tags with photos of each item
- Rack, shelf and yard location mapping inside the malkhana
- Chain-of-custody log for every handover
- Tracking of items sent to court and forensic labs
- Return, auction and destruction as per court orders
- Alerts for pending items, court dates and long-held property
- Audit, inventory and station-wise reports

## Challenges Before This Solution

Before this system, case property was tracked in thick handwritten registers, which made items hard to find, easy to lose and difficult to account for in court.

1. **Handwritten registers.** Entries were made by hand, often with incomplete descriptions. Old registers faded, got damaged or went missing.
2. **Items were hard to locate.** With thousands of items piled in the malkhana, finding one article for a court hearing could take hours.
3. **Weak chain of custody.** There was no reliable record of who took an item out, when it came back, or what condition it was in. This weakened evidence in court.
4. **Loss, theft and tampering.** Cash, jewellery and drugs went missing or were swapped, and it was hard to fix responsibility.
5. **Court and lab tracking was manual.** Items sent to court or the forensic lab were tracked on paper, so delays and missing returns went unnoticed.
6. **Overflowing malkhanas.** Property stayed for years after cases ended because nobody tracked disposal orders. Seized vehicles rusted in station yards.
7. **Slow returns to owners.** Rightful owners waited months to get back their vehicles or valuables, even after court orders.
8. **Transfers broke continuity.** When a malkhana in-charge was transferred, handover was slow and gaps in the inventory surfaced only later.
9. **No visibility for seniors.** Senior officers could not see pending property, disposal backlog or audit status across stations.

## The Solution

The system gives every seized item a digital identity, a fixed place and a complete history, from the day of seizure to its final return or disposal.

| Challenge | How the system solves it |
| --- | --- |
| Handwritten registers | Digital seizure form with FIR link, category, description, value and photos |
| Items were hard to locate | QR tag on every item, mapped to its rack, shelf or yard slot; scan or search to find it in seconds |
| Weak chain of custody | Every handover is logged with officer name, date, time, purpose and condition, with a scan at each step |
| Loss, theft and tampering | Approval workflow for every movement, photo checks on return and a full audit trail |
| Court and lab tracking was manual | Movement module tracks items sent to court or forensic lab and flags overdue returns |
| Overflowing malkhanas | Disposal module records court orders and lists items due for return, auction or destruction |
| Slow returns to owners | Owner details and court order captured, with a printable handover receipt |
| Transfers broke continuity | One-click charge handover report showing the full inventory |
| No visibility for seniors | Dashboard of pending, moved, disposed and long-held items across all stations |

**Core modules**

- **Seizure Entry** — register property against the FIR with photos, value and seizure details.
- **Tagging & Storage** — generate QR labels and assign a storage location.
- **Inventory** — search, filter and scan to see any item's status and location.
- **Movement & Custody** — issue and receive items for court, forensic lab or investigation.
- **Disposal** — return to owner, auction or destroy as per court order.
- **Alerts** — reminders for court dates, overdue returns and items held too long.
- **Reports & Audit** — inventory, custody history, disposal and station-wise reports.

## Flow Pages

The app runs in 10 pages that follow an item from seizure to storage, through court or lab visits, to final disposal.

&#91;embedded content: property lifecycle · 10 pages\]

An item can go out to court or the lab and come back many times; each trip is logged before it rejoins the inventory.

1. **Login** — Secure, role-based sign-in for investigating officers, malkhana in-charges, SHOs and senior officers.
2. **Dashboard** — Total items in custody, items in court or lab, upcoming court dates, pending disposals and alerts.
3. **Seizure Entry** — A form to record FIR or case number, seizure date and place, item category, description, quantity, estimated value, photos and witness details.
4. **Tagging and Storage** — The system generates a unique property ID and QR label, and the in-charge assigns a rack, shelf or yard slot.
5. **Inventory** — Search by FIR, category, date or ID, or scan a QR tag, to see an item's location, status and history.
6. **Movement Request** — The IO requests an item for court, forensic lab or investigation, with purpose and expected return date. The SHO approves it.
7. **Issue and Receive** — The in-charge scans the item out and back in, recording who took it, when, and its condition on return.
8. **Court Order** — The officer records the court's final order and uploads a copy.
9. **Disposal** — The item is returned to its owner, sent to auction or destroyed, with a receipt or certificate, and its record is closed.
10. **Reports and Audit** — Inventory, custody history, pending disposals, long-held property and station-wise reports, exportable to PDF and Excel.

## FAQs (Frequently Asked Questions)

**1. What is muddemaal?** Muddemaal is property seized by police as evidence or during an investigation, such as vehicles, cash, jewellery, weapons, drugs, phones and documents. It is stored in the police station's malkhana until the court decides its fate.

**2. Who uses the system?** Investigating officers, malkhana in-charges, station house officers and senior officers. Each role sees only the actions and data meant for it.

**3. How is each item identified?** Every item gets a unique property ID and a printed QR tag. Scanning the tag shows its details, photos, FIR, location and full custody history.

**4. What is chain of custody, and how does the system keep it?** Chain of custody is the record of everyone who handled an item. The system logs every issue and return with the officer, date, time, purpose and condition, so the record holds up in court.

**5. Can property be tracked when it goes to court or the forensic lab?** Yes. The movement module records where the item went, who carried it and the expected return date. Overdue items are flagged automatically.

**6. How is disposal handled?** Once the court passes an order, the officer records it in the system and chooses return to owner, auction or destruction. The item is closed with a receipt or disposal certificate.

**7. Does it handle vehicles and large items?** Yes. Vehicles are recorded with registration, chassis and engine numbers, photos and their parking slot in the station yard.

**8. What happens when the malkhana in-charge is transferred?** The system generates a full inventory handover report. The outgoing and incoming officers verify items by scanning, and any mismatch is recorded.

**9. Can old register entries be added?** Yes. Existing property from paper registers can be digitised in bulk, so the inventory is complete from day one.

**10. How is the data secured?** Through role-based access, approval for every movement, encrypted data and an audit trail that cannot be edited.

**11. What reports are available?** Inventory by category or case, custody history, items in court or lab, pending disposals, long-held property and station-wise summaries.
