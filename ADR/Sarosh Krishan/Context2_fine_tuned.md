# ADR: Message Queue as the Primary Data Store

## Decision
The system will use a Message Queue as the primary data store. This will ensure that the system can handle the high-frequency updates without any significant downtime.## Consequences: * Removes the need to handle giant files * Opens up the possibility of advanced analytics in the future * Allows for advanced scalability * Gives IoT devices priority access to the system * Moves data from backup to foreground usage * Helps with cost efficiency * Needed for mobile device connectivity ### Positive Consequences * The system will be able to handle large amounts
