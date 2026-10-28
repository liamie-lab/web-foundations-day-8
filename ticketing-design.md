
# TicketHub System Design

## 1. Requirements

### Functional Requirements

1. **User Registration and Login:** Users can create accounts and log in securely.
2. **Browse Events:** Users can view upcoming concerts and events, including dates, venues, prices, and ticket availability.
3. **View Seats:** Users can view available, held, and booked seats for an event.
4. **Hold Seats:** Users can temporarily reserve available seats while completing payment.
5. **Make Payments:** Users can pay for tickets using supported payment methods.
6. **Confirm Bookings:** The system confirms a booking only after successful payment.
7. **View Tickets:** Users can view and access their purchased tickets.
8. **Prevent Double-Booking:** The system must prevent two users from purchasing the same seat.
9. **Send Notifications:** Users receive booking confirmations and payment status updates.

### Non-Functional Requirements

1. **Speed:** Event pages and seat maps should load quickly, ideally within 2 seconds under normal traffic.
2. **Correctness:** A seat must never be sold to two different users. Bookings and payments must be processed reliably.
3. **Fairness:** Users should be treated fairly during popular ticket sales. The system should use a waiting queue to manage heavy traffic.
4. **Scalability:** The system must handle 50,000 daily visitors and sudden spikes of up to 200,000 people trying to buy tickets.
5. **Availability:** The system should remain accessible during high-demand events and recover quickly from failures.
6. **Security:** User accounts and payment information must be protected using authentication, encryption, and secure payment processing.
7. **Reliability:** Failed payments should not result in confirmed bookings, and users should receive accurate booking status updates.
8. **Maintainability:** The system should use separate components that can be updated and maintained independently.
