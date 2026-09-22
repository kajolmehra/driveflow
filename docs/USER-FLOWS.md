# User flows

```mermaid
flowchart TB
    Visitor[Browse courses and services] --> Lead[Register interest]
    Lead --> Verify[Verify email / OTP]
    Verify --> Select[Choose course, city, and slot]
    Select --> Enroll[Submit enrollment]
    Enroll --> Decision{School / vendor decision}
    Decision -->|Accepted| Fulfil[Deliver learning or service]
    Decision -->|Rejected| Amend[Show next action]
    Amend --> Select
    Fulfil --> Progress[Track progress / booking status]
    Fulfil --> Invoice[Generate invoice record]
    Vendor[Vendor workspace] --> Booking[Review service booking]
    Booking --> Status[Confirm, complete, or cancel]
    Status --> Settlement[Apply commission and payout state]
    Invoice --> Settlement
    Admin[Admin workspace] --> Rules[Configure prices and commission]
    Rules --> Settlement
```

## Commission and payout lifecycle

1. The platform resolves a course/service price for the selected city or vendor offering.
2. A commission rule is applied as a percentage or fixed amount.
3. The booking or enrollment retains the commercial metadata for admin review.
4. Eligible agent/vendor balances are summarized into payout records and invoices.
5. Admin actions mark payouts as paid while preserving an auditable history.
