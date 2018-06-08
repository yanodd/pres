
---
# Chapter 7

DDoS Detection

---
### Current Status

- Areas of interest identified
- Overview Done
- Work assigned

---
### Overview

```
Detection Methods
- Netflow
  - Summary
    - what is netflow
    - how does it work
    - what is required (exporter, collector)
    - versions (v6, MPLS)
    - interface direction
  - Placement
    - all interconnection/peering points: absolute minimum (for detecting attacks from the "outside"
    - hybrid: peering+core (catch a decent percentage of "inside" attacks also)
    - "near" customer routers (PE): extra, for same PoP attacks (src, dst in the same area)
  - Router Config
    - sampling ratio
    - timers, etc
    - interfaces (which and what direction)          
  - Pros
    - netflow is industry standard (supported by all and developed)
    - netflow is proven technology
    - netflow is "cheap" (in terms of CPU cycles)
    - netflow as a detection method is mature and proven           
  - Cons
    - up to L4 only (debatable disadvantage)
  - Key Points
    - ...
- Inline
  - Summary
    - bump-in-the-wire deployment
    - makes sense as a CPE device, not so much in the Core or Peerings
    - usually deployed as complimentary detection method for customers          
    - also covers application-layer attacks
  - Pros
    - up to L7
    - can protect...?

  - Cons
    - expensive (both in terms of money and CPU cycles)
    - cannot be used in core/peerings (DDoS vector in itself due to capacity limitation, SPoF)
    - cannot protect against volumetric attacks
  - Key Points
    - ...
- Mirrored
  - Summary
    - as in inline, this also is a complimentary (to Netflow) method of detection
    - usually, part of the traffic is mirrored and analysed, not all of it
  - Pros
    - up to L7
    - unlike inline, not a SPoF or attack vector
  - Cons
    - extra links needed in routers
    - extra processing in routers (policies for traffic selection)
  - Key Points
    - ...
```

---
### Next Steps

```
[1st draft]: TBD 
[Request For Comments]: internal
[Request For Comments]: external
```
