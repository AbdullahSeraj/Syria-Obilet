# Syrian Travel Platform
## README.md — System Architecture & Tech Stack

---

# Overview

This project is a full-scale Travel & Booking Platform similar to systems like Enuygun and Obilet, built to serve the Syrian market and later expand regionally.

It includes:

- Website (Next.js)
- Mobile App (optional future)
- Admin Dashboard
- Partner/Vendor Dashboard
- Backend APIs
- Payment & Booking Engine

The architecture is designed to be scalable, modular, and production-ready.

---

# System Architecture

The system follows a:

> Modular Monolith Architecture (Scalable to Microservices)

This means:
- One backend system initially
- Divided into independent modules:
  - Flights Module
  - Buses Module
  - Hotels Module
  - Chalets Module
  - Cars Rental Module
  - Payments Module
  - Users Module
  - Notifications Module

Each module is isolated in logic but shares the same infrastructure.

---

# Frontend Stack

## Next.js (Main Web Application)

- Server-Side Rendering (SSR)
- SEO-friendly for travel search pages
- Fast routing and performance optimization
- API integration with backend
- Dynamic pages for:
  - Flights search
  - Hotels listing
  - Bus tickets
  - Booking details

---

## Vite (Optional Admin / Internal Apps)

Used for:
- Admin dashboard (lightweight SPA)
- Partner dashboard
- Internal tools

Benefits:
- Fast development server
- Hot Module Replacement (HMR)
- Lightweight builds

---

## React.js

Core UI library used across:
- Admin panel
- Dashboard interfaces
- Reusable components system

---

## TailwindCSS

Used for styling:

- Utility-first CSS framework
- Fast UI development
- Responsive design support
- Consistent design system

---

## shadcn/ui

Modern UI component system:

- Pre-built accessible components
- Buttons, dialogs, tables, forms
- Fully customizable design system
- Works with TailwindCSS

---

## Routing

- Next.js file-based routing (Main Website)
- React Router (for Vite dashboards if needed)

Routing structure example:

- /flights
- /hotels
- /buses
- /booking/[id]
- /profile
- /admin/dashboard

---

# Backend Stack

## Node.js

Core backend runtime:

- High performance (event-driven architecture)
- Handles concurrent requests efficiently
- Ideal for booking systems

---

## Express.js / NestJS

Backend framework:

- REST API development
- Middleware handling
- Authentication system (JWT)
- Modular structure support

Recommended: NestJS for large-scale systems

---

## MongoDB

Primary database:

- Flexible schema for dynamic travel data
- High scalability
- Fast read/write operations
- Supports geo-data

Used for:
- Users
- Bookings
- Flights data
- Hotels data
- Payments logs
- Notifications

---

## Redis

Used for:

- Caching search results
- Sessions storage
- Fast performance
- Rate limiting
- Temporary booking locks

---

## BullMQ

Used for background jobs:

- Email sending
- SMS notifications
- Ticket generation
- Payment processing tasks

---

# Infrastructure & Deployment

## DigitalOcean

Used for hosting backend and databases:

- Droplets (servers)
- Managed MongoDB (optional)
- Load balancing
- Scaling options
- Firewall configuration

---

## Docker

Used for containerization:

- Backend services
- Database services
- Deployment consistency

---

## Nginx

Used as:

- Reverse proxy
- Load balancing
- HTTPS handling
- Domain routing

---

# Security

- JWT Authentication
- Refresh Tokens
- Role-Based Access Control
- OAuth login
- Rate limiting
- API protection middleware

---

# API Testing

## Postman

Used for:

- API testing
- Endpoint documentation
- Debugging workflows
- Collaboration between teams

---

# Key System Features

## Flight Booking System
- Search via APIs or GDS
- Price filtering
- Ticket generation

---

## Bus Booking System
- Seat selection
- QR ticket generation
- Real-time availability

---

## Hotels & Chalets
- Listings management
- Booking engine
- Availability calendar

---

## Payment System
- Multiple gateways
- Transaction logs
- Refund handling

---

## Notifications System
- Email notifications
- SMS alerts
- Push notifications

---

## Admin Dashboard
- Users management
- Bookings monitoring
- Revenue analytics
- Vendor management

---

## Vendor System
- Add services
- Manage pricing
- View bookings
- Revenue tracking

---

# Performance Strategy

- Redis caching
- Lazy loading
- SSR optimization
- Database indexing
- CDN usage
- Queue-based processing

---

# Scalability Plan

Phase 1
- Modular Monolith backend
- Single database

Phase 2
- Add caching and queues
- Multi-server deployment

Phase 3
- Convert to Microservices:
  - Flights Service
  - Hotels Service
  - Payments Service

---

# Summary

This stack is designed to build a high-performance travel booking platform capable of handling search, booking, payments, and multi-provider integrations with future scalability.