# 👤 Person Tracker Card for Home Assistant - EN

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)

Advanced card for Home Assistant that displays detailed information about people with complete visual editor.

![Person Tracker Card](images/preview.png)

## ✨ Key Features

- 📱 **Battery Monitoring** - Displays device battery level with dynamic icon
- 🚶 **Activity Tracking** - Shows current activity (Walking, Running, Automotive, Stationary, Cycling)
- 📍 **Distance from Home** - Waze integration to calculate distance
- ⏱️ **Travel Time** - Estimates time needed to reach home/work
- 📶 **Connection Type** - Shows if device is connected via WiFi or mobile network
- 🎨 **Customizable States** - Different colors and images for each state (Home, Office, etc.)
- 🖼️ **Custom Images** - Support for transparent PNG/GIF images
- 🎯 **Complete Visual Editor** - Easy configuration via graphical interface
- 📐 **Flexible Layout** - Freely position each element on the card
- 🎨 **Highly Customizable** - Fonts, colors, sizes, spacing completely configurable

## 📸 Screenshots

### Visual Editor
| Base Tab | Sensors Tab | States Tab |
|----------|-------------|-----------|
| ![Base Editor](images/editor-base.png) | ![Sensors Editor](images/editor-sensors.png) | ![States Editor](images/editor-states.png) |

## 📦 Installation

### HACS (Recommended)

1. Open HACS in your Home Assistant
2. Go to "Frontend"
3. Click on the three dots in the top right
4. Select "Custom repositories"
5. Add this URL: `https://github.com/djdevil/person-tracker-card`
6. Select category "Dashboard"
7. Click "Add"
8. Search for "Person Tracker Card" and install it
9. Restart Home Assistant

### Manual Installation

1. Download `person-tracker-card.js` and `person-tracker-card-editor.js`
2. Copy the files to the `config/www/person-tracker-card/` folder
3. Add the resource in Home Assistant:
   - Go to Settings → Dashboards → Menu (⋮) → Resources
   - Click "+ ADD RESOURCE"
   - URL: `/local/person-tracker-card/person-tracker-card.js`
   - Type: JavaScript Module
4. Reload the page (Ctrl+F5)

## 🔧 Basic Configuration

### Method 1: Visual Editor (Recommended)

1. Edit your dashboard
2. Add a new card
3. Search for "Person Tracker Card"
4. Configure through the graphical interface

### Method 2: YAML
```yaml
type: custom:person-tracker-card
entity: person.davide
show_entity_picture: true
show_name: true
show_last_changed: true
show_battery: true
show_activity: true
show_distance: true
show_travel_time: true
show_connection: true
```
# 👤 Person Tracker Card for Home Assistant - Italian Section (Translated)
## ✨ Key Features

- 📱 **Battery Monitoring** - Displays device battery level with dynamic icon
- 🚶 **Activity Tracking** - Shows current activity (Walking, Running, Automotive, Stationary, Cycling)
- 📍 **Distance from Home** - Waze integration to calculate distance
- ⏱️ **Travel Time** - Estimates the time needed to reach home/work
- 📶 **Connection Type** - Shows if the device is connected via WiFi or mobile network
- 🎨 **Customizable States** - Different colors and images for each state (Home, Office, etc.)
- 🖼️ **Custom Images** - Support for transparent PNG/GIF images
- 🎯 **Complete Visual Editor** - Easy configuration through the graphical interface
- 📐 **Flexible Layout** - Freely position every element on the card
- 🎨 **Highly Customizable** - Fonts, colors, sizes, and spacing are fully configurable

## 📸 Screenshots

### Visual Editor
| Base Tab | Sensors Tab | States Tab |
|----------|------------|----------|
| ![Base Editor](images/editor-base.png) | ![Sensors Editor](images/editor-sensors.png) | ![States Editor](images/editor-states.png) |

## 📦 Installation

### HACS (Recommended)

1. Open HACS in your Home Assistant
2. Go to "Frontend"
3. Click the three dots in the top right
4. Select "Custom repositories"
5. Add this URL: `https://github.com/djdevil/person-tracker-card`
6. Select category "Dashboard"
7. Click "Add"
8. Search for "Person Tracker Card" and install it
9. Restart Home Assistant

### Manual Installation

1. Download `person-tracker-card.js` and `person-tracker-card-editor.js`
2. Copy the files to the `config/www/person-tracker-card/` folder
3. Add the resource in Home Assistant:
   - Go to Settings → Dashboards → Menu (⋮) → Resources
   - Click "+ ADD RESOURCE"
   - URL: `/local/person-tracker-card/person-tracker-card.js`
   - Type: JavaScript Module
4. Reload the page (Ctrl+F5)

## 🔧 Basic Configuration

### Method 1: Visual Editor (Recommended)

1. Edit your dashboard
2. Add a new card
3. Search for "Person Tracker Card"
4. Configure through the graphical interface

### Method 2: YAML

```yaml
type: custom:person-tracker-card
entity: person.davide
show_entity_picture: true
show_name: true
show_last_changed: true
show_battery: true
show_activity: true
show_distance: true
show_travel_time: true
show_connection: true
```

## ⚙️ Advanced Configuration

### Full Options

```yaml
type: custom:person-tracker-card
entity: person.davide

# Element Visibility
show_entity_picture: true
show_name: true
show_last_changed: true
show_battery: true
show_activity: true
show_distance: true
show_travel_time: true
show_connection: true

# Custom Sensors (optional)
battery_sensor: sensor.phone_davide_battery_level
activity_sensor: sensor.phone_davide_activity
connection_sensor: sensor.phone_davide_connection_type
distance_sensor: sensor.waze_davide
travel_sensor: sensor.casa_lavoro_davide

# Layout and Dimensions
aspect_ratio: '1/0.7'
picture_size: 55

# General Styles
card_background: 'rgba(255,255,255,0.05)'
card_border_radius: '15px'
name_font_size: '20px'
state_font_size: '14px'

# Element Placement
battery_position: top-right
activity_position: bottom-left
distance_position: top-left
travel_position: top-left-2
connection_position: bottom-right

# Element Font Sizes
battery_font_size: '13px'
activity_font_size: '13px'
distance_font_size: '12px'
travel_font_size: '12px'
connection_font_size: '12px'

# Updates
triggers_update: all  # all | entity | custom

# Custom States (see below)
state:
  - value: home
    name: 🏡 Home
    styles:
      name:
        color: '#7DDA9F'
  - value: not_home
    name: 🏃‍♂️ Away
    styles:
      name:
        color: '#93ADCB'
```

### Custom States with Images

You can define custom states with different colors and images:

```yaml
state:
  - value: home
    name: 🏡 Home
    entity_picture: /local/images/home.png
    styles:
      name:
        color: '#7DDA9F'
  
  - value: Office
    name: 🏢 Office
    entity_picture: /local/images/office.png
    styles:
      name:
        color: '#FFD700'
  
  - value: Gym
    name: 🏋️ Gym
    entity_picture: /local/images/gym.gif
    styles:
      name:
        color: '#FF6B6B'
```

### Available Positions

Each element can be placed in one of the following positions:

- `top-left`
- `top-right`
- `bottom-left`
- `bottom-right`
- `top-left-2` (secondary slot)
- `top-right-2` (secondary slot)
- `bottom-left-2` (secondary slot)
- `bottom-right-2` (secondary slot)

### Update Modes

The `triggers_update` option controls when the card refreshes:

- `all` - Updates when any related entity changes (default)
- `entity` - Updates only when the main person entity changes
- `custom` - Updates for user-defined entities

## 🎨 Creating Custom Images

### With iPhone/iPad

1. **Download the free "Background Eraser" app**
   - Available on the App Store
   - Easy to remove backgrounds

2. **Create your image**:
   - Take a photo or use an existing picture
   - Open the Background Eraser app
   - Remove the background with your finger
   - Export as a transparent PNG

3. **For animated images (GIFs)**:
   - Use the free "ImgPlay" app
   - Create a GIF from photos or videos
   - You can also remove the background
   - Export as GIF

4. **Upload to Home Assistant**:
   - Copy the file to `config/www/images/`
   - Use the path `/local/images/yourimage.png` in your configuration

### Recommended Sizes

- **Static images (PNG)**: 512x512 px
- **Animated GIFs**: 512x512 px, max 5 MB
- **Format**: PNG with transparency or GIF
- **Background**: Transparent for best integration

### Image Ideas

Examples you can create:
- 🏠 Home - Your house logo
- 🏢 Office - Company logo
- 🏋️ Gym - Fitness icon
- 🛒 Grocery - Store logo
- 🚗 Traveling - Animated car icon
- ✈️ Airport - Airplane icon

## 📱 Home Assistant Companion App Integration

For proper operation, ensure the Home Assistant Companion app has permissions for:

1. **Location**:
   - Open phone settings
   - Apps → Home Assistant
   - Location → Always

2. **Battery**:
   - Tracked automatically by the app

3. **Physical activity**:
   - iOS: Settings → Privacy → Motion & Fitness
   - Android: Enable the activity sensor in the app

4. **Connectivity**:
   - Tracked automatically by the app

### Companion App Sensors Used

The card automatically looks for these sensors:

```
sensor.phone_[name]_battery_level
sensor.phone_[name]_activity
sensor.phone_[name]_connection_type
```

Where `[name]` is the person entity name without the `person.` prefix.

Example for `person.davide`:
```
sensor.phone_davide_battery_level
sensor.phone_davide_activity
sensor.phone_davide_connection_type
```

## 🗺️ Waze Integration

For distance from home, install the Waze Travel Time integration:

1. Go to Settings → Devices & Services
2. Add integration → Search for "Waze"
3. Configure:
   - Origin: Your home zone
   - Destination: `person.name`
   - Name: `waze_name`

## 🎭 Configuration Examples

### Minimal Configuration

```yaml
type: custom:person-tracker-card
entity: person.davide
```

### Full Configuration

```yaml
type: custom:person-tracker-card
entity: person.davide
show_entity_picture: true
show_name: true
show_last_changed: true
show_battery: true
show_activity: true
show_distance: true
show_travel_time: true
show_connection: true
aspect_ratio: '1/0.7'
picture_size: 60
card_background: 'linear-gradient(135deg, rgba(125, 218, 159, 0.1) 0%, rgba(147, 173, 203, 0.1) 100%)'
card_border_radius: '20px'
name_font_size: '22px'
state_font_size: '16px'
battery_position: top-right
activity_position: bottom-left
distance_position: top-left
travel_position: top-left-2
connection_position: bottom-right
state:
  - value: home
    name: 🏡 At Home
    entity_picture: /local/images/home.gif
    styles:
      name:
        color: '#7DDA9F'
  - value: Office
    name: 🏢 At the Office
    entity_picture: /local/images/office.png
    styles:
      name:
        color: '#FFD700'
  - value: not_home
    name: 🌍 Out and About
    entity_picture: /local/images/travel.gif
    styles:
      name:
        color: '#93ADCB'
```

### Essential Information Only

```yaml
type: custom:person-tracker-card
entity: person.davide
show_entity_picture: true
show_name: true
show_last_changed: true
show_battery: true
show_activity: false
show_distance: false
show_travel_time: false
show_connection: true
aspect_ratio: '1/0.5'
```

## 🔍 Troubleshooting

### Card does not appear

1. Check the browser console (F12) for errors
2. Verify that the resource is loaded correctly
3. Reload the page with an empty cache (Ctrl+Shift+R)

### Sensors are not found

1. Make sure the Companion app is installed and configured
2. Check sensor names in Developer Tools → States
3. Manually specify sensors in the configuration

### Custom images do not appear

1. Confirm the file is in `config/www/`

2. Use the correct path: `/local/folder/file.png`

3. Check file permissions
4. Restart Home Assistant if needed

### The editor does not open

1. Make sure both JS files are loaded
2. Reload Lovelace resources
3. Try restarting Home Assistant

## 📝 Changelog

### v1.0 (2024-11-22)
- 🎉 First public release
- ✨ Full visual editor
- 📱 Support for all Companion App sensors
- 🎨 Customizable states with colors
- 📍 Waze integration for distances


## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the project
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is released under the MIT License. See the [LICENSE](LICENSE) file for details.

## 💝 Support

If this card is useful to you, consider:

- ⭐ Starring the repository
- 🐛 Reporting bugs and issues
- 💡 Suggesting new features
- 🤝 Contributing code

## 🙏 Acknowledgements

- Home Assistant Community
- HACS Team
- All contributors

---

**Created with ❤️ for the Home Assistant community**
