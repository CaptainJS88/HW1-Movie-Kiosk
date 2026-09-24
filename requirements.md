# Movie Kiosk Requirements

| ID | Requirement | Priority |
| --- | --- | --- |
| R1 | The customer can view available movies and their showtimes. | Medium |
| R2 | The customer can choose an available seat for a selected showtime. | High |
| R3 | The customer can purchase a ticket for the selected showtime and seat. | High |
| R4 | The system provides a confirmation after a successful purchase. | Medium |
| R5 | The system prevents the same seat from being sold twice for the same showtime. | High |

## Acceptance criteria

- **R1:** Selecting a movie displays its available showtimes.
- **R2:** Only available seats for the selected showtime can be selected.
- **R3:** A successful payment creates one ticket for the selected showtime and seat.
- **R4:** The confirmation shows the ticket ID, movie, showtime, and seat number.
- **R5:** When two customers try to buy the same seat for the same showtime, at most one purchase succeeds. The same physical seat can be sold for different showtimes.

## Modeling assumptions

- Seat availability is specific to a showtime; in the domain model, `Seat` represents a seat offered for one showtime.
- The Ticket Service atomically checks and holds the selected seat before requesting payment. A successful payment converts that hold to a sale; a failed payment or an expired hold releases the seat.
- The sequence diagram shows the successful purchase path. Failure and timeout paths are described here rather than expanded in the diagram.
