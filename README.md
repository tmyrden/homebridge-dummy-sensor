# homebridge-dummy-sensor

`homebridge-dummy-sensor` is a plugin for Homebridge, designed to enhance your HomeKit automation by adding a combination switch & sensor accessory. This plugin draws inspiration from the `homebridge-dummy` plugin, while offering more versatility with HomeKit native notifications.

## Features

- **Linked Switch-Sensor Mechanism**: Toggling the switch changes the sensor's state, integrating seamlessly with HomeKit's notification system.
- **Customizable Sensor Types**: Choose between a contact sensor or a leak sensor, each with distinct notification behaviors in HomeKit.

## Example Configuration

Accessories can be defined following the schema formatting shown here:

```json
"accessories": [
    {
        "name": "Front Door Ajar",
        "type": "contact",
        "accessory": "DummyContactSensor"
    },
    {
        "name": "Back Door Ajar",
        "type": "leak",
        "accessory": "DummyContactSensor"
    }
]
```

### Configuration Fields

- `name`: The name of the sensor as it will appear in HomeKit.
- `type`: Type of sensor (`contact` for contact sensor, `leak` for leak sensor).
- `accessory`: Must be `"DummyContactSensor"`.

## Usage

Once configured, the plugin will create an accessory with both a switch and a sensor in HomeKit. Toggling the switch will change the state of the corresponding sensor, allowing for the triggering of HomeKit notifications.

- **Contact Sensor**: Provides standard notifications.
- **Leak Sensor**: Sends time-sensitive notifications, capable of breaking through any focus mode.

## Support

For issues, suggestions, or contributions, please open an issue or pull request.

## License

This project is licensed under the MIT License.