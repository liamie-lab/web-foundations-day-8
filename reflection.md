
# TicketHub System Design Reflection

Designing TicketHub helped me understand the challenges of building a ticket-booking system that can handle both normal traffic and sudden spikes during popular ticket sales.

One of the most important lessons I learned is that preventing double-booking requires more than checking whether a seat is available on the frontend. Multiple users may attempt to purchase the same seat at the same time. Database transactions, row-level locking, and unique constraints help ensure that only one user can successfully reserve a seat.

I also learned the importance of scalability. A system that works well on a normal day may struggle when thousands of people try to buy tickets simultaneously. Load balancing, caching, and a waiting queue can help manage heavy traffic and improve system reliability.

Another challenge is balancing speed with accuracy. Caching can make event information load faster, but seat reservations must use reliable database operations to avoid incorrect bookings. Payment processing also requires careful verification so that an order is confirmed only after successful payment.

If I were to improve this design further, I would add monitoring, automated testing, and recovery procedures for failed payments and server outages. I would also test the system under heavy traffic to identify performance bottlenecks.

Overall, this assignment improved my understanding of APIs, database relationships, system architecture, scalability, and reliable booking processes.
