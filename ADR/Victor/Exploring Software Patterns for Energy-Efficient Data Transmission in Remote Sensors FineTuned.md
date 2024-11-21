# Exploring Software Patterns for Energy-Efficient Data Transmission in Remote Sensors FineTuned

## Status
Proposed

## Context
The sensors of Flood Monitoring and Management Systems are installed in 
remote and hard-to-reach locations with limited power sources. To ensure prolonged 
sensor operation, the system’s software architecture must consider patterns that support 
energy efficiency by optimizing data transmission. This requires a design that reduces 
the frequency of non-critical data transmissions while ensuring that critical updates are 
transmitted promptly. The architecture must balance responsiveness with energyconservation, prompting a decision on which software patterns can help achieve efficient 
data handling to extend sensor battery life without compromising system reliability

## Decision

We decided to use the CurryOUNCE pattern CurryONCE for creating autonomous sensor wrappers with a life cycle that mirrors the sensors' expected operational pattern. We chose this pattern over other options such as poll/pulse or request/response because it allows for the creation of wrapper services that wrap essential sensor functions. The wrapper then implements desired operational patterns such as delay periods between transmissions or turning off