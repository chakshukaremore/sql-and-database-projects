# Celestial Bodies Database 🌌

A PostgreSQL relational database project that stores information about
galaxies, stars, planets, moons, and space probes.

## 📌 Project Overview

The database is named `universe` and contains multiple related tables
representing different celestial objects.

The project demonstrates relational database design using primary keys,
foreign keys, unique constraints, sequences, and structured data.

## 🗂️ Database Tables

### 🌌 Galaxy
Stores information about galaxies, including:
- Galaxy name
- Galaxy type
- Distance from Earth
- Whether it has life
- Description

### ⭐ Star
Stores information about stars, including:
- Star name
- Galaxy
- Age
- Spherical shape
- Spectral class

### 🪐 Planet
Stores information about planets, including:
- Planet name
- Star
- Distance from Earth
- Planet type
- Whether it has life
- Spherical shape

### 🌙 Moon
Stores information about moons, including:
- Moon name
- Planet
- Age
- Atmosphere
- Spherical shape

### 🚀 Space Probe
Stores information about space probes, including:
- Probe name
- Description
- Active status
- Cost

## 🔗 Database Relationships

The database uses foreign keys to establish relationships between
celestial objects:

```text
Galaxy
   ↓
 Star
   ↓
Planet
   ↓
Moon
