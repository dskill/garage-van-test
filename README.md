# Garage Van Clearance Visualizer

Interactive tool to determine if a tall van can safely enter a garage with a steep downward-sloping driveway.

## Problem Statement

When driving a tall vehicle (like a Nissan NV200 with a pop-top camper conversion) into a garage with a steep driveway ramp, there's a critical clearance concern: as the van descends the ramp, the vehicle tilts nose-down, which raises the rear of the vehicle. At the transition point where the front wheels reach the garage floor while the rear wheels are still on the ramp, the rear roofline may collide with the garage door header.

This is not obvious from static measurements alone. A van that appears to fit based on "van height < door height" may actually collide due to the geometry of the angled approach.

**This tool visualizes the exact clearance at every point of entry**, allowing you to:
- Input precise measurements of your vehicle and garage
- Animate the van through the entire approach
- Find the worst-case (minimum clearance) position automatically
- Determine if garage modifications are needed before committing to construction

## Usage

Open `index.html` in a browser, or run a local server:

```bash
python3 -m http.server 8000
# Open http://localhost:8000
```

## Measurements

All inputs support both metric and imperial:
- Enter values in mm (e.g., `1860`)
- Enter values in inches with quotes (e.g., `73"` or `73in`)

### Key Parameters

**Van:**
- Overall height (ground to top of roof/pop-top when closed)
- Wheelbase, ground clearance, front/rear overhang
- Wheel diameter

**Garage:**
- Entrance height (floor to bottom of header)
- Header depth (thickness of the header beam)

**Driveway:**
- Ramp angle (degrees) - the slope going down into the garage
- Ramp length (horizontal distance from street to garage floor)

## Defaults

Pre-configured for a Nissan NV200 with pop-top approaching a specific garage:
- Van height: 1860 mm (73.2")
- Entrance height: 2108 mm (83.0")
- Ramp angle: 10.4°
- Ramp length: 3302 mm (130.0")

## License

MIT
