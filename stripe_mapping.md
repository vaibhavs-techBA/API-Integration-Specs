# Stripe Multi-Currency API Integration & Ledger Mapping

## 1. Objective
Migrate single-currency checkout to support 10+ localized currencies via Stripe. Ensure 100% data parity between Stripe webhooks and our internal database.

## 2. API Schema Mapping
**Endpoint:** `POST /v1/payment_intents`

Mapped JSON payload fields from frontend checkout to Stripe API:
*   `amount` (Integer) -> Mapped to `txn_amount` in DB.
*   `currency` (String) -> Mapped to `currency_code` (e.g., 'usd', 'eur').
*   `metadata.order_id` (String) -> Mapped to `internal_order_uuid` to maintain relational integrity.

## 3. Validation Strategy
I built SQL validation scripts to audit daily cross-border transactions, identifying floating-point or currency-conversion discrepancies before UAT. This automation saved the engineering squad ~20 manual audit hours per week.
