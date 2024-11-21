# ADR: Event-Based Architecture for FMMS

## Decision
We will use a celebratory event-based architecture that removes the need for continuous polling. With this approach, data is only sent to the server when there is a significant change in the ecological landscape, such as a rise in water level or a drop in temperature. By not continuously sending incremental data, the antenna avoids overloading the channel with irrelevant information that drains the battery faster. This event-based approach is more appropriate in a system where data is not continuous, but instead, it is event-based, as
