# My Bali — Itinerary, Route, and Transport Intelligence

**Status:** Exploratory concept; no algorithm or fare model approved.

## Purpose
Help users create journeys that are feasible in the real world while allowing custom routes that differ from common tourist itineraries. Explain the practical implications of a choice rather than automatically rejecting unusual routes.

## Potential inputs
- Arrival/departure dates and times, airport or port, accommodation, and anchor locations.
- Places and activities selected by the user.
- Preferred visit windows and expected duration.
- Venue operating hours and provider-reported availability.
- User preferences, budget, passenger/luggage needs, and transport preferences.
- Traffic and route estimates when reliable data is available.

## Itinerary feasibility
Evaluate travel distance/time, schedule conflicts, opening hours, activity duration, availability, backtracking, and cost implications. When a plan is impractical, explain the conflict and offer alternatives.

An unusual route is not automatically wrong. For example, a user may choose Kintamani to Uluwatu on the same day. The system should estimate the travel implications and let the user decide.

## Transport estimate concept
A future estimate may consider pickup/drop-off, distance, duration, vehicle category, passenger and luggage needs, waiting, stops, time-based surcharges, and provider-defined prices.

Clearly distinguish:
- Indicative estimate.
- Provider-confirmed quote.
- Booking request.
- Confirmed booking.
- Completed/fulfilled service.

Never invent a fare or imply that a provider has accepted a journey without confirmation.

## Availability sources
Availability may be manually updated, provider-confirmed, synchronized from provider systems, or returned by a supported live integration. The interface must disclose freshness and reliability. A listing does not imply availability.

## Open questions
Data sources, traffic reliability, opening-hour maintenance, provider availability synchronization, route calculation, fare logic, and responsibility for inaccurate estimates require research and design.
