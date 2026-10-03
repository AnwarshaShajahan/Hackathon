# HireD: Phase 1 MVP: Product Requirements Document

| | |
|---|---|
| **Version** | 0.2 (updated after first review) |
| **Status** | Verified|
| **Date** | 30 Sep 2026 |
| **Scope** | Phase 1|

---

## 1. Overview

### 1.1 Problem
The B2B process, from order intake through trip execution, invoicing and reporting, runs manually today. This makes it slow, hard to track, and prone to billing and payout errors.

### 1.2 Product Vision
HireD moves the existing B2B process onto a platform **without changing how the team already works**. Partner companies place and track orders, admins manage the operation, and drivers run trips and see their earnings, all in one system.

### 1.3 Goals
1. Digitize the complete flow: order → trip → payout → month-end invoice.
2. Give B2B partners self-service ordering and trip tracking.
3. Automate payout calculation so driver and company shares are always consistent.
4. Ensure invoices are checked by two people before reaching a partner.

### 1.4 Success Metrics
| Metric | Target (initial) |
|---|---|
| Orders placed through the B2B portal vs. phone/WhatsApp | Majority via portal |
| Closed trips with correct automatic payout | 100% |
| Month-end invoices verified by two users before sending | 100% |
| Time from order received to driver assigned | Tracked as baseline |

---

## 2. Users and Roles

| Role | Surface | Access |
|---|---|---|
| **Admin** | Web | Full visibility over orders, trips, drivers, companies, payroll, invoices and reports. Phase 1 has no permission tiers: all admin accounts have the same access. At least two admin accounts must exist to support two-person verification. |
| **B2B Partner** | Web portal | Own company's data only: create orders, track trips, view trip reports and verified statements. |
| **Driver** | Mobile app | Own data only: onboarding, assigned trips, expenses, history, wallet. |

---

## 3. Scope

### 3.1 In Scope
- **Admin Web Portal:** orders inbox, accept/reject, ongoing trips, driver directory and assignment, driver onboarding queue, company management, payroll settings, invoice verification, reports.
- **B2B Business Portal:** login, create order, order/trip tracking with time estimation, trip reports and month-end statements.
- **Driver Mobile App:** login, document upload, availability, trip list and detail, selfie, trip start, expenses, OTP trip close, trip history, document update, wallet.
- **Automation:** trip report on trip close, automatic driver payout to wallet, month-end statement consolidation.

### 3.2 Out of Scope (Not in this release)
- Formal driver document verification or approval checklist
- Automated commission-rate determination (rates are set manually by Admin)
- Automated omni-channel booking (e.g. WhatsApp bot creating orders)
- Multi-admin roles and permissions
- In-app payment gateway (B2B partners pay HireD directly, outside the platform)
- Driver accept/reject of assigned trips

---

## 4. End-to-End Flow

```
Order received (B2B portal, or admin-logged from phone/WhatsApp)
   ↓
Admin accepts or rejects ── Rejected → partner notified by email, order closed
   ↓ Accepted
Order becomes a Trip
   ↓
Admin assigns a driver (can reassign any time)
   ↓
Driver sees the trip in the app (no accept/reject step)
   ↓
Trip ongoing: selfie → start → expenses logged → OTP close
   ↓
Trip Report auto-generated (visible to partner)
   ↓
Driver share auto-calculated and credited to Driver Wallet on trip close
   ↓
Month end: closed trips consolidated into a Statement/Invoice
   ↓
Two-person verification (any two admin users)
   ↓
Statement/Invoice made available to partner in the B2B portal
   ↓
Payment settled directly between HireD and partner (outside the platform)
```

### 4.1 Order and Trip Statuses 
| Entity | Statuses |
|---|---|
| Order | Received → Accepted / Rejected |
| Trip | Unassigned → Assigned → Ongoing → Closed |
| Invoice | Draft → Pending Verification (creator + one other admin) → Verified → Published |
| Payout | Pending → Credited |

---

## 5. Functional Requirements

Priority: **P0** = must-have, **P1** = important, **P2** = nice-to-have.

### 5.1 B2B Business Portal

| ID | Requirement | Priority |
|---|---|---|
| B-01 | Partner logs in with credentials created by Admin; sees only their own company's data. | P0 |
| B-02 | Partner creates a new order with pickup, drop, date/time, vehicle/service notes and contact details. | P0 |
| B-03 | "My Orders/Trips" lists current and past orders with status. | P0 |
| B-04 | Each order/trip shows an estimated time (ETA/duration).  Calculated from pickup/drop via a maps service; Admin can override. | P1 |
| B-05 | Trip Report is viewable after the trip closes. | P0 |
| B-06 | Month-end statement/invoice is viewable only after two-person verification. | P0 |
| B-07 | Partner receives an email when an order is rejected. Also on acceptance and when a statement is published. | P1 |

**Acceptance (B-02):** Given a logged-in partner, when they submit a valid order, it appears in their list as *Received* and in the Admin inbox.

### 5.2 Admin Web Portal

| ID | Requirement | Priority |
|---|---|---|
| A-01 | Admin logs in with a secure account. | P0 |
| A-02 | Orders/Enquiries Inbox lists incoming orders from the B2B portal and admin-logged phone/WhatsApp requests. | P0 |
| A-03 | Admin can manually create an order on behalf of a company (for phone/WhatsApp requests). | P0 |
| A-04 | Order Detail page shows full information before the decision. | P0 |
| A-05 | Accept converts the order to a trip. Reject closes it and emails the partner. Admin confirms or sets the trip amount on acceptance; editable until the trip closes. | P0 |
| A-06 | Ongoing Trips page shows live list of in-progress trips with status. | P0 |
| A-07 | Driver Directory lists onboarded drivers with availability (online/offline and calendar). | P0 |
| A-08 | Assign Driver: Admin assigns a driver to an accepted trip and can reassign at any time. | P0 |
| A-09 | Driver Onboarding Queue shows new applications and uploaded documents. Admin marks a driver *Active* (accept-and-assign only, no verification workflow). | P0 |
| A-10 | Company Management: add and edit B2B partner records (name, contact person, contact details, address, other info), create partner login, and set the company's payout split (driver % / company %, e.g. 30 / 70) when the company is added. The split is mandatory. | P0 |
| A-11 | Payroll Settings: Admin can view and edit each company's payout split at any time. Rates are set manually and apply to trips closed after the change. | P0 |
| A-12 | Invoice Verification: two-person check on each month-end statement before it is sent. Approval comes from the admin who created the statement plus one other admin. | P0 |
| A-13 | Reports Dashboard (see 5.5). | P1 |

**Acceptance (A-08):** Assigning or reassigning a driver updates the trip immediately and the driver's trip list reflects the change.

### 5.3 Driver Mobile App

| ID | Requirement | Priority |
|---|---|---|
| D-01 | Driver logs in with basic credentials. | P0 |
| D-02 | Onboarding document upload: Driver License, Aadhar Card, PAN Card, Police Clearance Certificate (PCC). | P0 |
| D-03 | Availability: (a) online/offline toggle; (b) calendar to mark upcoming days available/unavailable in advance. | P1 |
| D-04 | Trip List shows trips assigned to this driver. | P0 |
| D-05 | Trip Detail shows pickup/drop and trip info. No accept/reject action. | P0 |
| D-06 | Selfie upload for identity confirmation as part of the trip flow. | P1 |
| D-07 | Trip Start begins an assigned trip and sets status to Ongoing. | P0 |
| D-08 | Expense Update: driver logs trip expenses before closing. Not a separate step afterward. | P0 |
| D-09 | Trip Close via OTP, allowed only after expenses are logged. Simple numeric code entry. The system generates a code per trip, shown to the partner in the portal, who gives it to the driver. | P0 |
| D-10 | Trip History lists past completed trips. | P1 |
| D-11 | Profile/Document Update to change submitted documents after onboarding. | P2 |
| D-12 | Driver Wallet shows balance and per-trip credits, updated automatically on trip close. Display-only; no in-app withdrawal. | P0 |

**Acceptance (D-09):** Given all expenses logged, when the driver enters the correct code, the trip closes, the report is generated and the wallet is credited. A wrong code shows an error and the trip stays open.

### 5.4 Payroll, Wallet and Invoicing

**Payroll rules**
- **The payout rate is set per company** as a driver % / company % split (example: Driver 30% / Company 70%). It is entered when the company is added in Company Management and can be edited later in Payroll Settings.
- There is no per-driver rate. Every driver on a company's trips receives that company's driver percentage.
- When creating or accepting a trip, Admin only enters the **total trip amount**; the split is applied automatically from the company's rate.
- The system never sets or changes rates on its own.
- Each trip stores the rate applied at close, so later rate edits never change past trips.

**Automatic payout on trip close**

| Example: Trip amount ₹10,000 | Share | Amount |
|---|---|---|
| Driver | 30% | ₹3,000 |
| Company | 70% | ₹7,000 |
| **Total** | 100% | ₹10,000 |

- The driver's amount is credited to the Driver Wallet immediately on trip close, without waiting for the partner's payment.
- Expenses are recorded and shown in the trip report but are not part of the commission split.

**Trip Payroll Record (per closed trip):** Trip ID, Driver, B2B Partner, trip amount, applied rate, driver share, company share, total, payment status, payout/wallet status.

**Month-end Statement/Invoice**
- Admin triggers generation per company for a calendar month; it includes all *Closed* trips in that month.
- Contents: total trip amount, total driver share, total company share, trip-wise rates and monthly totals.
- **Two-person verification [Confirmed]:** the statement must be approved by the admin who created it and by one other admin. Both approvals are recorded (who, when) before it can be published.
- After verification, the statement appears in the partner's portal.
- Payment is settled outside the platform. No payment page or gateway.

**Principle:** Admin sets the rule → trip completes → system calculates → wallet updated → report updated → month-end statement → two-person verification → partner access.

### 5.5 Reports (Admin)

| Report | Description |
|---|---|
| Billing issues | Discrepancies between trip and invoice data |
| Driver delay report | Drivers who delay trips most often |
| Client order volume and success rate | Orders per company and on-time delivery rate |
| Driver payout report | Per-driver payouts, updating as trips close |
| Trip Report | Filter: live / daily / monthly |
| Order Report | Orders with status and outcome |
| Driver (Staff) Work Report | Trips and activity per driver |

---

## 6. Data Model (High Level)

| Entity | Key fields |
|---|---|
| Company | name, contact person, contact details, address, payout split (driver % / company %) |
| Order | company, pickup, drop, date/time, notes, status, source (portal/admin) |
| Trip | order, driver, amount, ETA, status, OTP, selfie, timestamps |
| Driver | profile, documents, availability, active status |
| Expense | trip, driver, amount, description |
| Wallet Transaction | driver, trip, amount, timestamp |
| Trip Payroll Record | as defined in 5.4 |
| Statement/Invoice | company, month, totals, status, verifier 1, verifier 2 |

---

## 7. Non-Functional Requirements

- **Security:** authenticated access on all three surfaces; partners and drivers can only access their own data.
- **Audit:** log changes to company payout splits, trip amounts, driver reassignment and invoice verification (who, what, when).
- **Reliability:** payout calculation runs exactly once per closed trip (no duplicate wallet credits).
- **Usability:** Driver App usable on common Android devices with low-bandwidth tolerance; admin and partner portals responsive on desktop.
- **Storage:** secure storage for uploaded documents and selfies.
- **Design:** built against separately prepared wireframes and base colour theme. This PRD defines function, not look.

---

## 8. Assumptions, Risks and Open Questions

### 8.1 Decisions and Assumptions
**Confirmed**
1. Admin sets or confirms the trip amount at acceptance.
2. Payout rate is set per company as a driver % / company % split (e.g. 30 / 70) when the company is added. Admin enters only the total trip amount per trip, and the split is applied automatically on trip close.
3. OTP is system-generated, shown to the partner, and entered by the driver.
4. Month-end verification is by the statement's creator plus one other admin.
5. Wallet is display-only; driver cash-out happens offline.
6. Two or more admin accounts exist, all with the same access.

**Still assumed (to be clarified by the team)**
1. Expenses are excluded from the payout split.
2. Admin triggers month-end invoice generation.
3. ETA is calculated by a maps service with admin override.
4. Rate edits apply only to trips closed afterward.

### 8.2 Risks
| Risk | Mitigation |
|---|---|
| Wrong rate or amount leads to wrong payouts | Audit log, and payout preview for the admin |
| Payout credited but partner never pays | Accepted business risk in Phase 1; visible in reports |
| Unverified driver documents | Accepted limitation; admin can view all documents |
| Low driver app adoption | Simple flow, minimal steps per screen |

### 8.3 Open Questions
- Who decides the trip price before Admin confirms it: the partner, or Admin alone?
- Should drivers or partners receive push/SMS/email alerts, and for which events?
- Are expenses reimbursed to the driver, and how?
- What happens to a trip if no driver is available?
- What should the "live" Trip Report mean: an auto-refreshing list of ongoing trips?

---

## 9. Release Readiness (Definition of Done)

- A partner can place an order, and Admin can accept it, assign a driver, and follow it to closure.
- A driver can complete a trip end to end and see the wallet credit.
- A month-end statement can be generated, verified by two admins, and viewed by the partner.
- All P0 requirements pass their acceptance criteria.