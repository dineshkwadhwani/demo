# ChoreVerse Context

## Working Product Name
- Current project name in this demo: ChoreVerse
- Umbrella concept: UtilityVerse (name can evolve)
- Positioning: one platform, many utility services, one entry point per service

## Product Vision
- Build a modern SaaS platform for utility service providers.
- Start with Laundry as the first utility.
- Expand later to other services such as cobbler and raddi-wala style services.
- Primary users are service businesses and their customers.
- Usage focus is mobile-first, while also supporting laptops.

## Core Multi-Tenant Model
- Each Laundry Service Provider is a tenant.
- Platform owner acts as SuperAdmin.
- SuperAdmin creates and manages TenantAdmins.
- TenantAdmins manage a portfolio of assigned service provider tenants.
- Each service provider manages their own coworkers and customer base.

## Roles
- SuperAdmin
- TenantAdmin
- ServiceProvider
- ServiceProvider Coworker
- Customer

## SuperAdmin Responsibilities
- Define and manage platform service catalog (bouquet of services).
- Create and manage TenantAdmins.
- Assign service providers to TenantAdmins.
- Control features (turn on/off by configuration).
- View reports across platform.
- Release payments to service providers.

## TenantAdmin Responsibilities
- Handle service provider onboarding after self-registration.
- Activate service providers after onboarding checks.
- Configure tenant profile and business details:
  - Logo and brand details
  - Owner details and contact information
  - Business profile details
  - GST and bank details
  - Enabled services from catalog
- Manage assigned tenant portfolio.

## ServiceProvider Responsibilities
- Manage own menu/services, pricing, and media.
- Configure operating hours and contact setup.
- Add/remove coworkers.
- Manage customer creation and customer linking rules.
- Receive and respond to order notifications.
- Confirm orders.
- Track payment receipts.
- Complete orders after payment.

## ServiceProvider Coworker Rules
- Coworker is always tied to creating ServiceProvider tenant.
- Coworker loses access if removed by ServiceProvider.

## Customer Responsibilities and Journey
- Customer may be added by ServiceProvider.
- Customer receives SMS with web link and app download link.
- Customer logs in with OTP.
- Customer sees linked ServiceProvider by default.
- Customer can request adding another ServiceProvider; approval required by TenantAdmin.
- Customer creates order.
- ServiceProvider receives notification and confirms.
- ServiceProvider can add services and attach images/videos per service item.
- Order can be marked completed once payment is done.

## Business Intent Notes
- Platform should reduce easy churn of customers away from provider.
- Payment flow confidence is critical for provider trust.
- UX must be very easy, intuitive, attractive, and age-friendly (roughly 11 to 80).

## High-Level Functional Flow
1. ServiceProvider self-registers (inactive).
2. SuperAdmin assigns provider to TenantAdmin.
3. TenantAdmin onboards and activates provider.
4. Provider configures services/menu/team/customers.
5. Customer places order.
6. Provider confirms and fulfills order.
7. Payment collected and order completed.

## Open Questions To Finalize Next
- Final brand decision: keep ChoreVerse, UtilityVerse, or new umbrella/sub-brand model?
- Will each service be a separate app shell or a module under one app?
- What are required KYC and compliance fields by tenant geography?
- Who owns customer lifecycle transitions (link/unlink approvals) in edge cases?
- What payment rails and payout schedule logic are expected?
- What notification channels are mandatory at launch (SMS, WhatsApp, push, email)?
- Which reports are needed for each role at MVP?
- What exact feature toggles should SuperAdmin control at launch?

## Next-Phase Planning Buckets
- Functional requirements and user stories by role.
- Information architecture and data model.
- Multi-tenant security and access control strategy.
- Technology architecture and deployment approach.
- Prototype UX flows (mobile-first plus laptop admin views).