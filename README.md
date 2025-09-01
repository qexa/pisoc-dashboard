# PiSOC Management Dashboard

## Overview

This project is a web-based management dashboard for PiSOC (Raspberry Pi Mini Security Operations Center), a cybersecurity lab environment that integrates multiple security tools including ELK Stack SIEM, Suricata IDS, Cowrie honeypot, and packet capture capabilities. The dashboard provides real-time monitoring, configuration management, attack simulation, and analytics for security professionals and students to manage and interact with their mini SOC infrastructure.

The application serves as a centralized control plane for cybersecurity operations, offering both educational value and practical security monitoring capabilities in an affordable, portable lab environment.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React.js with TypeScript for type safety and modern component development
- **Styling**: TailwindCSS with shadcn/ui component library for consistent, dark-themed cybersecurity interface
- **State Management**: TanStack Query (React Query) for server state management and real-time data synchronization
- **Routing**: Wouter for lightweight client-side routing
- **Real-time Updates**: WebSocket integration for live security feeds and status updates

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript for full-stack type safety
- **API Design**: RESTful API architecture with JSON responses
- **Development**: Hot module replacement via Vite for rapid development cycles
- **Build System**: ESBuild for production bundling with platform-specific optimizations

### Data Storage Solutions
- **Primary Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Database Provider**: Neon Database serverless PostgreSQL for scalable cloud storage
- **Schema Management**: Drizzle Kit for migrations and schema versioning
- **Session Storage**: Connect-pg-simple for PostgreSQL-backed session management

### Security Services Integration
- **Service Management**: Direct integration with systemd for controlling security services (Elasticsearch, Logstash, Kibana, Suricata, Cowrie)
- **Configuration Management**: Web-based editors for security tool configurations with syntax highlighting and validation
- **Real-time Monitoring**: Live feeds from security services with alert correlation and display
- **Attack Simulation**: Built-in tools for generating test traffic and validating security detections

### Data Processing Pipeline
- **Log Collection**: Integration with Filebeat and Logstash for centralized log aggregation
- **Alert Processing**: Real-time alert feed from Suricata IDS with severity classification
- **Honeypot Data**: Cowrie session tracking with geographic IP mapping and command logging
- **Metrics Collection**: System resource monitoring (CPU, memory, disk, network) with historical trending

## External Dependencies

### Database Services
- **Neon Database**: Serverless PostgreSQL hosting for production data storage
- **Drizzle ORM**: Type-safe database operations and query building

### Security Infrastructure
- **ELK Stack**: Elasticsearch, Logstash, Kibana for SIEM functionality
- **Suricata**: Network intrusion detection system for threat monitoring
- **Cowrie**: SSH/Telnet honeypot for attack behavior capture
- **Filebeat**: Log shipping agent for centralized log collection

### UI Framework Dependencies
- **Radix UI**: Accessible component primitives for complex UI interactions
- **Lucide React**: Icon library for consistent iconography
- **React Hook Form**: Form management with validation
- **Embla Carousel**: Touch-friendly carousel components

### Development Tools
- **Vite**: Build tool and development server with HMR support
- **TypeScript**: Static type checking across the entire stack
- **TailwindCSS**: Utility-first CSS framework for rapid styling
- **PostCSS**: CSS processing with autoprefixer for browser compatibility

### Network and System Integration
- **Systemd Integration**: Service control and status monitoring for Linux services
- **Network Monitoring**: tcpdump/Wireshark integration for packet capture analysis
- **Geographic IP Services**: IP geolocation for attack source visualization
- **File System Access**: Configuration file management and log file access
