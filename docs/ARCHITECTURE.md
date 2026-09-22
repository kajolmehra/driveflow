# Architecture

Driveflow is a Laravel API and React client organized by business role. Sanctum protects API sessions while route groups scope learner, school, vendor, agent, and administrator actions. Domain models cover courses, city pricing, enrollments, mock tests, service bookings, commissions, and payouts.

## Operational boundaries

- **Catalog:** courses, products, services, cities, prices, and availability.
- **Enrollment:** learner identity, OTP verification, course selection, schedules, progress, ratings, and invoices.
- **Marketplace:** vendor verification, service bookings, booking status, commission rules, and vendor payable calculation.
- **Agent network:** referral enrollments, per-course/city commission rules, payout records, and downloadable invoices.
- **Operations:** admin snapshots, notifications, moderation, exports, and live updates through Reverb/Pusher.
