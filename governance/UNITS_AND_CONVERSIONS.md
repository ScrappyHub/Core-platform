# 📏 CORE — UNITS & CONVERSIONS (CANONICAL V1)

Authority Level: Binding Platform Spec
Effective Date: First Public CORE Deployment
Status: ✅ LOCKED | ✅ BINDING | ✅ NON-OPTIONAL

## 1) Canonical Units (Mandatory)
All engines MUST emit unit-tagged quantities using these canonical units:

### Atmospheric
- Wind speed: m/s
- Rain rate: mm/hr
- Snow rate: mm/hr SWE (Snow Water Equivalent)

### Distance & Geometry
- Distance: meters (m)
- Scaling factor: distance_scale_factor ∈ {0.25, 0.50, 0.75, 1.00}

### Time
- Seconds (s)

### Temperature
- Kelvin (K) canonical

### Frequency
- Hertz (Hz)

### Pressure
- Pascal (Pa)

### Energy / Power
- Joule (J)
- Watt (W)

## 2) Display Conversions (Allowed, Not Canonical)
Engines MAY include display conversions in an explicit display block, but canonical MUST remain present:
- Wind: mph, kph display allowed (canonical remains m/s)
- Distance: feet/miles display allowed (canonical remains meters)

## 3) Unit Tagging Rule (Mandatory)
Every numeric output MUST be accompanied by:
- value
- unit
- (optional) reference_frame

Example:
{
  "wind_speed": { "value": 12.4, "unit": "m/s" }
}
