# PRODUCT SPECIFICATION (PRD) & AI CONTEXT

## 1. Project Overview
A mobile-first, gamified web application (PWA) for board game enthusiasts. The platform serves as a community hub where users can track their personal board game collections, organize local or online events, and build reputation within their local gaming community.

## 2. Core Problem & Solution
**Problem:** Organizing board game sessions is chaotic. Players struggle to find groups for specific heavy or niche games, keep track of who owns what, and deal with flaky participants who cancel at the last minute.
**Solution:** A centralized platform that combines collection management (via external integrations) with a structured event-planning system. A built-in reputation and gamification system ensures accountability and rewards active, reliable community members.

## 3. Target Audience & Roles
1. Guest: Can browse public events and leaderboards in a specific city, view gamified landing pages.
2. Verified Player: Can sync their collection, join events, earn achievements, and track their annual gaming activity.
3. Event Host: A player who creates events, sets rules, approves/declines participants, and manages the session lifecycle.
4. Admin/Moderator: Can manage reports, adjust reputation scores in dispute cases, and oversee regional leaderboards.

## 4. Key Features (MVP)
* **Gamified Collection Management:** Users can search and add games (e.g., Dune: Imperium, The Witcher: Old World) using the BoardGameGeek API. Visualized as customizable virtual shelves.
* **Event Creation & Discovery:** Hosts can create sessions specifying time, location (e.g., Lviv or online), game title, difficulty level, link to rules, and specific table rules. 
* **Reputation & Accountability System:** A dynamic rating system affected by attendance. No-shows or late cancellations without valid reasons negatively impact the score. Successful hosting and participation yield positive points and profile leveling.
* **Activity Tracking (GitHub-style):** A visual contribution graph showing a user's gaming activity over the year, shareable as a public profile component.
* **City Leaderboards:** Rankings for the most active hosts and players in specific regions.

## 5. Technical Architecture & Constraints
* **Frontend:** Next.js (App Router), React, SCSS (strict rule: NO Tailwind), Material UI / Mantine components. Highly optimized web animations for the gamification aspects. Must be fully PWA compliant.
* **Backend:** Node.js with TypeScript. Preferred framework: NestJS (to leverage strict OOP, DI, and system design principles) or Fastify+tRPC. 
* **Database & ORM:** PostgreSQL managed via Drizzle ORM.
* **Infrastructure:** Architecture must be designed for zero-cost scalability (Free Tier optimization). Vercel for frontend, Supabase/Neon for DB, Render/Railway for backend services. 
* **API Integrations:** BoardGameGeek (BGG) XML API for fetching game metadata and images.

## 6. System Design Guidelines for AI
When generating code or architecture for this project, the AI must prioritize:
1. Community-driven privacy (clear separation between public profiles and private data).
2. Efficient database queries to support the gamification and reputation engines without heavy compute loads.
3. Strict TypeScript typing across the entire stack.
4. Component reusability following Material v3 design principles via SCSS modularity.

## 7. Intellectual Property & Licensing
* **Proprietary Content:** This specification outlines a unique product concept and system design. It is shared strictly for informational and educational review.
* **Strict Restrictions:** Any copying, modification, or distribution of this document or the concepts within is prohibited without explicit written consent signed by the author.
* **Full Terms:** Please refer to the [LICENSE](LICENSE.md) file in the root of this repository for comprehensive licensing policies.
