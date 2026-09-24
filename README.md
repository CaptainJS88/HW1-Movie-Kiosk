# Movie Theater Ticket Kiosk

A movie theater kiosk lets customers view movies and showtimes, choose a seat, and buy a ticket. It gives a confirmation after the purchase and prevents the same seat from being sold twice for the same showtime. This repository contains the requirements and UML diagrams for Homework 1.

## Expanded use case: Purchase Ticket

**Primary Actor:** Customer

**Precondition:** The kiosk is working and showtimes are available.

**Main Steps:**

1. The customer chooses a movie and showtime.
2. The kiosk displays the available seats.
3. The customer selects a seat.
4. The Ticket Service checks whether the seat is available for that showtime.
5. The customer enters payment details, and the Payment Service processes the payment.
6. After payment is approved, the Ticket Service creates the ticket and marks the seat as sold.
7. The kiosk displays the ticket confirmation.

**Postcondition:** The customer has a confirmed ticket. The seat is marked as sold and cannot be sold again for the same showtime.

## UML diagrams

- [Domain model](diagrams/Movie-Kiosk-Domain-Model.png) · [Editable draw.io source](diagrams/Movie-Kiosk-Domain-Model.drawio)
- [Use-case diagram](diagrams/Movie-Kiosk-Use-Case.png) · [Editable draw.io source](diagrams/Movie-Kiosk-Use-Case.drawio)
- [Purchase-ticket sequence](diagrams/Purchase-Ticket-Sequence.png) · [Editable draw.io source](diagrams/Purchase-Ticket-Sequence.drawio)

## Work tracking

The five requirements are listed in [GitHub Issues](https://github.com/CaptainJS88/HW1-Movie-Kiosk/issues). The [Movie Kiosk Homework board](https://github.com/users/CaptainJS88/projects/1) tracks the homework items using To Do, In Progress, and Done.
