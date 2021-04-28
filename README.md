# EventQ
App to create and manage events

# Requirements
 - Event CRUD
 - Event comment
 - Event join
 - Map with precise location of the event
 - Push notification about when the event starts
 - Area based events
 - Chat
 - Report sistem

# Structure
 - Cloud hostable
 - Use of microservices
 - Google / fb auth
## Definitions
### Microservice manager
 - Service that exposes routes to child services
 - Handles several types of services
    * Event services (add/edit/join/delete)
    * User services (comment/message/inveite/chat)
### Event service type
 - Storage Service
   * Stores event schema
   * Performs the actual db querries
   * Other services highly dependant on this service
   * ** Minimize need of changes as much as possible
 - Data fetcher service
 - Data editor service
   * Service that checks user onto an event
   * Service that edits an event
   * Service that adds an event
