# API Integration Specs & Mapping

## Overview
This repository contains a sample Technical Business Analyst deliverable: an API mapping specification and Product Requirements Document (PRD) for integrating a multi-currency payment gateway (Stripe).

## Key Contents
* **API Schema Mapping:** Details the exact JSON payload fields (e.g., `amount`, `currency`, `metadata.order_id`) and how they map to the internal database schema.
* **Validation Strategy:** Outlines the SQL-based validation approach used to ensure 100% data parity before UAT.
* **Edge Cases:** Documents how the system handles failed webhooks, currency conversion floating-point errors, and missing metadata.

## Core File
* `stripe_mapping.md` - The full PRD and API schema mapping document.

## Purpose
This serves as a template for how a Technical BA bridges the gap between frontend checkout flows, third-party APIs, and backend database architecture.
