# FestivalFlow

A Spring Boot backend for managing music festivals end to end — from creating an event, to artists submitting performances, to staff handling the logistics behind the scenes.

I built this to go beyond basic CRUD and actually model how a festival works in practice: different people need different levels of access (an artist shouldn't be able to edit someone else's performance slot, but an organizer needs to see everything), and a lot of the real complexity is in the details — rehearsal slots, technical/setup requirements, merchandise — not just "festival has a name and a date."

## What it does

**Authentication & roles**
JWT-based authentication with role-based access control across five roles: Admin, Organizer, Staff, Artist, and User. Each role sees and can do different things — an Artist manages their own performances, an Organizer manages the festival itself, Staff handles operational details, and so on.

**Festival management**
Create, update, and browse festivals, with search and pagination so the API stays usable as the number of festivals and performances grows — not just a flat list dump.

**Performance booking**
Artists can submit performances for a festival and manage their own bookings, rather than an admin having to do it manually for everyone.

**Operational details**
Beyond the obvious (who's playing, when), the system tracks the things that actually make a festival run: technical/setup requirements per performance, merchandise, and rehearsal slot scheduling.

**Frontend**
A dark-themed, responsive web interface on top of the API, so the project isn't just endpoints in Postman — it's something you can actually click through.

## Tech stack

- **Backend:** Java, Spring Boot
- **Security:** Spring Security, JWT
- **API design:** RESTful, with pagination and search support
- **Frontend:** Server-rendered / responsive UI (dark theme)

## Why I built it this way

The interesting problem here wasn't the CRUD — it was the access control. Festivals genuinely have different stakeholders with different needs, and modeling that with a single role wouldn't reflect how it actually works. Splitting into five roles meant thinking through, for each endpoint, exactly who should be allowed to do what — which is closer to how you'd actually design a system for a real client than a typical student project.

## Running it locally

```bash
git clone https://github.com/hkokk1234/festivalflow.git
cd festivalflow
./mvnw spring-boot:run
```

*(Add your specific DB config / application.properties setup here once you confirm the exact steps.)*

## Possible next steps

- Automated tests for the booking and role-permission logic
- Payment integration for ticket/merchandise purchases
- Email notifications for booking confirmations
