# ServiceDesk

A multi-tenant application for managing IT support tickets and tracking equipment. Each organization can manage its own support queues, service-level policies, and asset inventory.

## What it does

- Organizes tickets into queues and tracks response and resolution deadlines.
- Keeps an asset inventory alongside support requests.
- Includes Active Directory and LDAP support through a separate directory sync agent.

## Code and architecture

| Area | Location |
| --- | --- |
| Next.js application and routes | [src/app](src/app) |
| Authentication, tenant scoping, and shared services | [src/lib](src/lib) |
| PostgreSQL data model | [prisma/schema.prisma](prisma/schema.prisma) |
| Active Directory sync agent | [ad-sync-agent](ad-sync-agent) |

## Local development

Use a supported Node.js release, npm, and a local PostgreSQL database. Configure the app with your own development database and credentials before starting it.

- Run `npm install` to install dependencies.
- Run `npm run db:generate` to generate the Prisma client.
- Run `npm run db:migrate` against your development database.
- Run `npm run dev` to start the Next.js development server.
