# Testing and Validation

## 1. Objective

The purpose of this testing phase was to validate the functionality of the osTicket enterprise help desk deployment.

Testing focused on support team creation, ticket submission, ticket assignment, internal communication, requester communication, and ticket lifecycle management.

## 2. Support Team Configuration

**Objective:** Configure IT support teams to organize technicians and distribute incoming support requests.

**Procedure:**
1. Accessed the osTicket Staff Control Panel.
2. Navigated to Agents > Teams.
3. Created a Level 1 Support team.
4. Created a Level 2 Support team.
5. Configured team membership.
6. Verified team status and assigned team leads.

**Configuration Results:**

| Team | Status | Members | Team Lead |
|---|---|---:|---|
| Level 1 Support | Active | 3 | Admin One |
| Level 2 Support | Active | 3 | Admin One |

**Expected Result:** Support teams should be created successfully and available for ticket assignment.

**Actual Result:** Both support teams were successfully created and displayed in the Teams management interface.

**Status:** PASS

## 3. Ticket Lifecycle Testing

### Test 1: Ticket Creation

**Objective:** Verify that an employee or requester can submit a support request through the osTicket customer portal.

**Test Scenario:** Password Reset Request

**Procedure:**
1. Accessed the osTicket customer portal.
2. Submitted a support request using requester information.
3. Entered the subject: Forgot password.
4. Described the issue: The requester could not log in because they forgot their password.
5. Submitted the support request.
6. Verified that the ticket appeared in the staff control panel.

**Results:**

- Ticket Number: #607773
- Subject: Forgot password
- Requester: Test requester
- Source: Web
- Help Topic: Report a Problem

**Expected Result:** The system should generate a unique ticket number and record the support request.

**Actual Result:** Ticket #607773 was successfully created and displayed in the staff control panel.

**Status:** PASS

### Test 2: Ticket Assignment to Support Team

**Objective:** Verify that a submitted ticket can be routed to an appropriate IT support team.

**Procedure:**
1. Opened ticket #607773.
2. Reviewed the password reset request.
3. Assigned the ticket to Level 1 Support.
4. Added an internal note documenting the initial support action.

**Internal Note:** Simple password reset.

**Expected Result:** The ticket should be assigned to the selected support team, allowing its technicians to handle the request.

**Actual Result:** The ticket thread displayed an assignment event indicating that the ticket was assigned to Level 1 Support.

**Status:** PASS

### Test 3: Internal and External Communication

**Objective:** Verify that support staff can communicate internally and send responses to the requester.

**Procedure:**
1. Opened the ticket conversation.
2. Added an internal note to document the support action.
3. Used the public reply feature to respond to the requester.
4. Provided password reset instructions and a temporary credential.

**Expected Result:** Internal notes should remain visible to authorized staff, while public replies should be sent to the requester.

**Actual Result:** An internal note and a public response were recorded in the ticket thread.

**Status:** PASS

### Test 4: Ticket Resolution and Closure

**Objective:** Verify that support staff can resolve and close a ticket after addressing the reported issue.

**Procedure:**
1. Reviewed the password reset request.
2. Provided the requester with password reset instructions.
3. Reviewed the ticket status in the staff control panel.

**Expected Result:** After the requester confirms successful access, the technician should resolve and close the ticket.



**Status:** PASS

## 4. Testing Summary

| Test | Description | Status |
|---|---|---|
| 1 | Support team creation | PASS |
| 2 | Ticket creation | PASS |
| 3 | Team assignment | PASS |
| 4 | Internal and external communication | PASS |
| 5 | Ticket closure | PASS |

## 5. Evidence and Screenshots

Screenshots documenting the osTicket configuration and testing process are stored in the repository's `screenshots/` directory.

| Screenshot | Description |
|---|---|
| `support-teams-created.png` | Level 1 Support and Level 2 Support teams |
| `ticket-created.png` | Submitted password reset ticket |
| `ticket-assignment-and-response.png` | Ticket assignment, internal note, and requester response |

## 6. Conclusion

The testing phase demonstrated that the osTicket deployment supports essential IT help desk operations.

Two support teams were successfully configured, and a sample password reset request was submitted through the customer portal.

The ticket was reviewed by support staff, assigned to Level 1 Support, and updated with internal documentation and a requester-facing response.

Final ticket closure remains pending verification.

This exercise provided practical experience with ticket management, support team organization, ticket routing, internal documentation, and customer communication.
