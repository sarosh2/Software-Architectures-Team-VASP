# ADR: Hybrid Data Transmission Strategy

## Decision
TTo effectively manage energy consumption while ensuring timely updates for critical data, we will implement a hybrid data transmission strategy that incorporates event-driven and batch processing patterns.

## Rationale
1. **Event-Driven Updates**: The system will prioritize event-driven notifications for critical data that require immediate attention (e.g., water levels exceeding a threshold, alerts for potential flooding). This ensures that important updates are transmitted without delay, thus maintaining system reliability and responsiveness.
2. **Batch Processing**: Non-critical data transmissions (e.g., routine status updates or readings that fall within safe ranges) will be aggregated and transmitted at predefined intervals. This approach reduces the frequency of data transmissions, effectively conserving battery life by minimizing the power expended in radio usage and increasing the overall operational lifespan of the sensors.
3. **Adaptive Frequency**: The architecture will support an adaptive transmission frequency mechanism that can vary the batch intervals based on environmental conditions or historical data patterns. For instance, during stable weather conditions, the system can increase the interval between batch updates, while during periods of significant weather change, it can decrease the interval to ensure more frequent data collection.
4. **Sensor Sleep Mode**: Implementing sleep modes during periods of inactivity will further enhance energy savings. Sensors can enter a low-power state when not actively collecting critical data, waking only when necessary based on certain triggers (such as external command or sensor readings reaching a predefined state).

## Benefits
By utilizing this hybrid strategy, we can achieve a balance between responsiveness and energy conservation, ensuring that the Flood Monitoring and Management System operates efficiently in remote locations while maintaining critical alerting capabilities. This approach not only supports the longevity of the sensor batteries but also enhances the overall reliability of flood monitoring efforts.
