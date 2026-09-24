# Movie Theater Ticket Kiosk

A self-service movie theater kiosk lets a customer view available movies and showtimes, choose an available seat, and purchase a ticket. The system confirms a successful purchase and prevents the same seat from being sold twice for the same showtime.

This repository contains requirements and UML models for a guided software engineering tools exercise. No software implementation is required.

## Expanded use case: Purchase Ticket

**Primary Actor:** Customer

**Precondition:** The kiosk is available, at least one movie showtime is offered, and the customer has a supported payment method.

**Main Steps:**

1. The customer views the available movies and selects a showtime.
2. The kiosk requests and displays the available seats for that showtime.
3. The customer selects a seat and requests a ticket purchase.
4. The Ticket Service atomically checks that the seat is available and places a temporary hold on it.
5. The customer provides payment details, and the Payment Service processes the payment.
6. After payment approval, the Ticket Service records the ticket and marks the held seat as sold for that showtime.
7. The kiosk displays a confirmation with the ticket ID, movie, showtime, and seat number.

**Postcondition:** One paid ticket exists for the customer, the selected seat is sold for that showtime, and the customer has received confirmation. Another purchase cannot sell that same seat for the same showtime.

**Exceptions:** If the seat is already held or sold, the kiosk asks the customer to select another seat. If payment fails, no ticket is issued and the seat hold is released.

## UML diagrams

- [Domain model](diagrams/Movie-Kiosk-Domain-Model.png) · [Editable draw.io source](diagrams/Movie-Kiosk-Domain-Model.drawio)
- [Use-case diagram](diagrams/Movie-Kiosk-Use-Case.png) · [Editable draw.io source](diagrams/Movie-Kiosk-Use-Case.drawio)
- [Purchase-ticket sequence](diagrams/Purchase-Ticket-Sequence.png) · [Editable draw.io source](diagrams/Purchase-Ticket-Sequence.drawio)

## Work tracking

The [requirement issues](https://github.com/CaptainJS88/HW1-Movie-Kiosk/issues) use `requirement` and priority labels. The [Movie Kiosk Homework board](https://github.com/users/CaptainJS88/projects/1) demonstrates To Do, In Progress, and Done for this modeling exercise.
