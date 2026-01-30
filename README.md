# RescueNet Pro

A mesh networking app for emergency communication using BLE and WiFi Direct.

## Overview

RescueNet Pro enables peer-to-peer communication in disaster scenarios where traditional networks are unavailable. It uses a hybrid approach combining Bluetooth Low Energy (BLE) for long-range discovery and WiFi Direct for high-throughput data transfer.

## Features

- **SOS Emergency Messaging** - Send location-tagged distress signals
- **Mesh Networking** - Messages relay through multiple devices
- **Hybrid Connectivity** - Automatic BLE/WiFi switching
- **Offline Support** - Message queue for when connectivity is restored
- **AI-Powered Routing** - Q-Learning based path optimization

## Architecture

```
lib/
├── core/                 # Shared Foundation
│   ├── constants/        # BLE UUIDs, app configs
│   ├── errors/           # Custom exceptions
│   └── network/          # Network adapter interface
│
├── data/                 # Hardware & Storage Layer
│   ├── datasources/
│   │   ├── ble/          # BLE implementation
│   │   ├── wifi/         # WiFi Direct implementation
│   │   └── local_db/     # Hive storage
│   ├── repositories/     # Repository implementations
│   └── hybrid_manager.dart
│
├── domain/               # Business Logic (Pure Dart)
│   ├── entities/         # Data models
│   ├── repositories/     # Abstract interfaces
│   └── usecases/         # Business actions
│
├── presentation/         # UI Layer
│   ├── bloc/             # State management
│   ├── pages/            # Screens
│   └── widgets/          # Reusable components
│
└── main.dart             # App entry point
```

## Getting Started

1. Clone the repository
2. Run `flutter pub get`
3. Run `flutter run`

## Requirements

- Flutter 3.0+
- Android 8.0+ (for WiFi Direct)
- iOS 13+ (BLE only)

## License

MIT License
