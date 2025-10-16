# 🚀 FiveM Installation Guide for ox_inventory

## 📋 Prerequisites

Before installing ox_inventory, ensure you have the following dependencies:

### Required Dependencies
- **FiveM Server** (Build 6116 or higher)
- **OneSync** enabled
- **oxmysql** - Database connector
- **ox_lib** - Core library system

### Supported Frameworks
- ✅ **ox_core** (Recommended)
- ✅ **ESX** (esx_core)
- ✅ **QBox** (qbx_core) 
- ✅ **ND Core** (ND_Core)

## 🔧 Installation Steps

### 1. Download & Extract
```bash
# Download the latest release
wget https://github.com/Provokke/ox-inventory/archive/refs/tags/v2.44.1-fivem-ready.zip

# Extract to your resources folder
# Place in: resources/[ox]/ox_inventory/
```

### 2. Database Setup
```sql
-- Run the SQL file provided with ox_inventory
-- This creates the necessary tables for inventory data
```

### 3. Server Configuration

#### server.cfg
```cfg
# Add to your server.cfg
ensure oxmysql
ensure ox_lib
ensure ox_inventory

# OneSync is required
set onesync on
```

#### Resource Load Order
```cfg
# Ensure proper load order in server.cfg
start oxmysql
start ox_lib
start [ox]  # This will start ox_inventory
```

### 4. Framework Integration

#### For ESX Users
```lua
-- No additional configuration needed
-- ox_inventory automatically detects ESX
```

#### For QBox Users  
```lua
-- ox_inventory has native QBox support
-- Ensure qbx_core is loaded before ox_inventory
```

#### For ox_core Users
```lua
-- Optimal performance with ox_core
-- Full feature compatibility
```

## ⚙️ Configuration

### Basic Configuration
Edit the configuration files in the `data/` folder:
- `data/items.lua` - Item definitions
- `data/shops.lua` - Shop configurations  
- `data/stashes.lua` - Stash locations
- `data/vehicles.lua` - Vehicle inventory settings

### Performance Optimization
```lua
-- In fxmanifest.lua (already configured)
fx_version 'cerulean'
use_experimental_fxv2_oal 'yes'
lua54 'yes'
```

## 🎮 Features Ready for FiveM

### ✨ Core Features
- **Slot-based inventory system** with drag & drop UI
- **Weapon system** with attachments and ammo
- **Shop system** with currency support
- **Stash system** with access controls
- **Vehicle inventories** (gloveboxes, trunks)
- **Item durability** and metadata support

### 🔒 Security Features
- Server-side validation for all interactions
- Anti-cheat protection built-in
- Secure item handling and logging
- Permission-based access controls

### 🎨 User Interface
- Modern, responsive web UI
- Real-time inventory synchronization
- Multi-language support (25+ languages)
- Customizable themes and layouts

## 🚨 Troubleshooting

### Common Issues

#### "ox_lib not found"
```bash
# Ensure ox_lib is installed and started before ox_inventory
ensure ox_lib
ensure ox_inventory
```

#### "Database connection failed"
```bash
# Check oxmysql configuration
# Ensure database credentials are correct in oxmysql config
```

#### "UI not loading"
```bash
# Verify web build exists
# Check console for JavaScript errors
# Ensure proper resource permissions
```

### Performance Issues
- Enable OneSync for optimal performance
- Use SSD storage for faster loading
- Allocate sufficient server memory (4GB+ recommended)

## 📚 Additional Resources

- **Documentation**: https://overextended.dev/ox_inventory
- **Original Repository**: https://github.com/overextended/ox_inventory
- **This Fork**: https://github.com/Provokke/ox-inventory

## 🆘 Support

For support and questions:
1. Check the official documentation first
2. Search existing GitHub issues
3. Create a new issue with detailed information

## 📄 License

This project is licensed under the GNU General Public License v3.0
See LICENSE file for details.

---

**Version**: v2.44.1-fivem-ready  
**Last Updated**: January 2025  
**Compatibility**: FiveM Build 6116+