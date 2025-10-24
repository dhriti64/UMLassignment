# Association Data-Structure Table


| Association (A ↔ B) | Multiplicity (A..B) | Owning Class | Concrete DS + Var Name | Notes/Purpose |
|---|---|---|---|---|
| User ↔ Forum (via Membership) | User *..* Forum | **Forum** | `ArrayList<Membership> memberships` | Forum maintains member links. |
| User ↔ Membership | User 1..* Membership | **User** | `ArrayList<Membership> memberships` | Backref to a user’s memberships. |
| Forum ↔ Thread | Forum 1..* Thread | **Forum** | `ArrayList<Thread> threads` | Composition: threads owned by forum. |
| Thread ↔ Message | Thread 1..* Message | **Thread** | `ArrayList<Message> messages` | Composition: messages owned by thread. |




| Association (A ↔ B) | Multiplicity (A..B) | Owning Class | Concrete DS + Var Name | Notes/Purpose |
|---|---|---|---|---|
| User ↔ Message (author) | User 1..* Message |  |  |  |
| Forum ↔ Invitation (outgoing) | Forum 1..* Invitation |  |  |  |
| Invitation ↔ User (recipient) | Invitation 1 ↔ User 1 |  |  |  |
| Forum ↔ Owner (User; must be a Member) | Forum 1 ↔ User 1 |  |  |  |
| Forum ↔ Moderator (User; must be a Member) | Forum 1 ↔ User 1 |  |  |  |
| Forum ↔ Message (pending-review helper) | Forum 0..* Message |  |  |  |

