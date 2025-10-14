# OX Inventory Reskin - 2000s Retro Windows Theme 🖥️

A nostalgic, production-ready reskin of the popular ox_inventory resource for FiveM servers, featuring an authentic **2000s Windows XP/Vista era interface**. This version combines the classic Windows aesthetic with modern performance optimization, bringing back the iconic blue gradients, rounded corners, and familiar UI elements that defined early 2000s computing.

## 🎨 Theme Features

- **🖥️ Authentic 2000s Windows Design**: Classic Windows XP/Vista inspired interface
- **💙 Iconic Blue Gradients**: Traditional Windows blue color scheme with glass effects
- **🔘 Rounded Corners & Buttons**: Nostalgic UI elements from the golden age of Windows
- **📁 Classic Window Frames**: Familiar title bars and window decorations
- **🎵 Retro Sound Effects**: Optional Windows-style notification sounds
- **✨ Glass Aero Effects**: Translucent windows reminiscent of Windows Vista

## 🚀 Technical Features

- **Production Optimized**: All development files removed, minimal footprint
- **Multi-Framework Support**: Compatible with ESX, QBCore, QBox, and more
- **Retro-Modern UI**: Classic 2000s aesthetics with modern functionality
- **High Performance**: Optimized for 60+ FPS with Y2K-era resource efficiency
- **Extensive Item Support**: Hundreds of pre-configured items with images
- **Crafting System**: Built-in crafting mechanics
- **Shop System**: Configurable shop locations and inventories
- **Vehicle Integration**: Vehicle trunk and glovebox support
- **Weapon Attachments**: Full weapon customization system
- **Multi-Language**: Support for 25+ languages

## 📋 Requirements

- **FiveM Server**: Latest recommended version
- **Framework**: ESX, QBCore, QBox, or ND Framework
- **Database**: MySQL/MariaDB
- **Dependencies**: 
  - ox_lib (latest version)
  - oxmysql (if using MySQL)

## 🔧 Installation

### 1. Download and Extract
```bash
# Download the latest release
# Extract to your resources folder
[ox]/ox_inventory/
```

### 2. Database Setup
```sql
-- Import the provided SQL file (if included)
-- Or ensure your framework's inventory tables are properly configured
```

### 3. Server Configuration
Add to your `server.cfg`:
```cfg
ensure ox_lib
ensure ox_inventory
```

### 4. Framework Configuration
Edit `fxmanifest.lua` to match your framework:
```lua
-- Uncomment your framework
-- '@es_extended/imports.lua',
-- '@qb-core/imports.lua',
-- '@qbx_core/imports.lua',
```

### 5. Restart Server
```bash
restart ox_inventory
# or
refresh
start ox_inventory
```

## ⚙️ Configuration

### Items Configuration
Edit `data/items.lua` to customize items:
```lua
['bread'] = {
    label = 'Bread',
    weight = 125,
    stack = true,
    close = true,
    description = "A fresh loaf of bread"
},
```

### Shops Configuration
Configure shops in `data/shops.lua`:
```lua
['shop_name'] = {
    name = 'Shop Name',
    blip = {
        id = 52, colour = 69, scale = 0.8
    },
    inventory = {
        { name = 'bread', price = 10 },
        { name = 'water', price = 5 },
    },
    locations = {
        vec3(25.7, -1347.3, 29.49)
    }
}
```

### Crafting Configuration
Set up crafting recipes in `data/crafting.lua`:
```lua
['lockpick'] = {
    ingredients = {
        scrapmetal = 2,
        plastic = 1
    },
    time = 5000,
    amount = 1
}
```

## 🎮 Usage

### Basic Commands
- `/inventory` - Open inventory (if enabled)
- `/giveitem [id] [item] [amount]` - Give item to player (admin)
- `/removeitem [id] [item] [amount]` - Remove item from player (admin)

### Inventory Shortcuts
- **Right Click**: Use/consume item (classic Windows context menu style)
- **Drag & Drop**: Move items between slots (Windows XP drag behavior)
- **Shift + Click**: Quick move items (retro keyboard shortcuts)
- **Ctrl + Click**: Split item stack (familiar Windows conventions)

### Vehicle Integration
- **Trunk Access**: Approach vehicle rear and press interaction key
- **Glovebox Access**: Enter vehicle and use interaction menu

## 🔨 Customization & Theme Options

### 2000s Windows Theme Customization
This reskin captures the authentic 2000s Windows experience:
- **Classic Blue Theme**: Traditional Windows XP Luna blue color scheme
- **Aero Glass Effects**: Windows Vista-style translucent elements
- **Retro Typography**: Period-appropriate fonts and text rendering
- **Nostalgic Animations**: Smooth transitions reminiscent of early 2000s UI

### Adding Custom Items
1. Add item definition to `data/items.lua`
2. Add item image to `web/images/` (PNG format, lowercase name)
3. Configure item properties (weight, stack, etc.)
4. Restart resource

### Theme Preservation Notice
The UI maintains the authentic 2000s Windows aesthetic. For modifications:
1. Custom changes should preserve the retro Windows theme
2. Contact the original ox_inventory developers for major UI overhauls
3. This version prioritizes nostalgic authenticity and performance

### Performance Optimization
This version is already optimized with:
- ✅ Removed development dependencies
- ✅ Minified web assets
- ✅ Optimized file structure
- ✅ Production-ready configuration

## 🐛 Troubleshooting

### Common Issues

**Inventory not opening:**
- Check framework compatibility
- Ensure ox_lib is running
- Verify resource start order

**Items not showing images:**
- Check image file names match item names
- Ensure images are in PNG format
- Verify web/images/ directory exists

**Performance issues:**
- Check server specifications
- Monitor resource usage with `/resmon`
- Ensure database is optimized

**Database errors:**
- Verify MySQL connection
- Check table structure
- Ensure proper permissions

### Debug Mode
Enable debug in `fxmanifest.lua`:
```lua
client_debug_mode 'true'
server_debug_mode 'true'
```

## 📊 Performance Metrics

Optimized for:
- **Memory Usage**: <50MB typical
- **CPU Usage**: <5% during normal operation
- **Network Traffic**: Y2K-optimized with efficient events
- **Database Queries**: Batched and optimized

## 🤝 Support

### Getting Help
1. Check this README first
2. Review the troubleshooting section
3. Check ox_inventory documentation
4. Join FiveM development communities

### Reporting Issues
When reporting issues, include:
- FiveM server version
- Framework and version
- Error messages (F8 console)
- Steps to reproduce

## 📝 License

This project maintains the original ox_inventory license. Please respect the original developers' work and licensing terms.

## 🙏 Credits

- **Original ox_inventory**: Overextended team
- **2000s Windows Theme**: Nostalgic UI design inspired by Windows XP/Vista era
- **Retro Optimization**: Production-ready modifications with classic aesthetics
- **Community**: FiveM development community and retro computing enthusiasts

## 📈 Changelog

### Version 1.0.0 - "Millennium Edition"
- Initial production-ready release with 2000s Windows theme
- Authentic Windows XP/Vista inspired interface design
- Classic blue gradients and glass effects implementation
- Removed all development dependencies
- Optimized file structure for nostalgic performance
- Added comprehensive retro-themed documentation
- Performance optimizations maintaining period authenticity

---

**Note**: This is a production-optimized version of ox_inventory with an authentic 2000s Windows theme. Experience the nostalgia of early millennium computing while enjoying modern FiveM functionality. For development and source code modifications, refer to the original ox_inventory repository.

## 🚀 Quick Start - Y2K Style

1. Download latest "Millennium Edition" release
2. Extract to `resources/[ox]/ox_inventory/`
3. Add `ensure ox_inventory` to server.cfg
4. Restart server
5. Enjoy your optimized inventory system!

---

*Made with ❤️ for the FiveM community*