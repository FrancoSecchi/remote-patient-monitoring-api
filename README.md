# Remote Patient Monitoring API

Backend for monitoring chronic patients at home. Devices send readings (blood pressure, glucose, heart rate…), the API checks them against each patient's limits, and the care team gets an alert when something is out of range.

> **Status:** in progress — v1 started October 2026.
> All data is synthetic. This is a learning project, not a medical device.

## The problem

A home-care coordinator follows dozens of chronic patients. Today, readings arrive scattered (phone calls, photos, spreadsheets) and an out-of-range value can go unnoticed for days. This project is built as if for that (fictional) client: one place where readings land, are validated, and turn into alerts the right person sees.

## Scope — v1

- [ ] **Patients and measurement types**, with limits defined per patient and per type (a 150 mmHg reading can be normal for one patient and an alert for another)
- [ ] **Alerts** inside the system when a reading crosses a limit
- [ ] **Roles:** coordinator, doctor, nurse — each sees and does different things
- [ ] **History and averages** per patient and measurement type
- [ ] **Device ingestion** with duplicate detection (devices retry; the same reading must not be stored twice)

Out of scope for v1: real devices, notifications outside the system (email/SMS), frontend (React, planned later).

## Stack

| Layer | Choice |
|---|---|
| API | FastAPI, Pydantic |
| Persistence | SQLAlchemy 2.0, PostgreSQL |
| Tests | pytest |
| Infra | Docker, GitHub Actions, Render |

## Running locally

_Coming soon_ — `docker compose up` + seed with synthetic patients.

## Design decisions

_Coming soon_ - Key decisions and their trade-offs are recorded in [`docs/decisions/`](docs/decisions/) as they're made.
