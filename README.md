# Phase Noise to RMS Jitter Converter

A free, browser-based tool that converts single-sideband phase noise data L(f) (dBc/Hz vs. offset frequency) into integrated RMS jitter and RMS phase noise — built for OCXO, TCXO and crystal oscillator evaluation in RF and timing system design.

**Online tool: <https://xiaokeni2.github.io/phase-noise-jitter-converter/>**

## Formula

```
RMS jitter = sqrt( 2 · ∫ 10^(L(f)/10) df ) / (2π · f0)
```

where:

- `L(f)` — single-sideband phase noise in dBc/Hz at offset frequency `f`
- `f0` — carrier (oscillator) frequency
- integration limits `f1`–`f2` default to 12 Hz – 1 MHz, a typical OCXO integration bandwidth, and are fully configurable

L(f) is piecewise-linearly interpolated on a logarithmic frequency axis between the entered points; outside the entered offset range, the slope of the nearest segment is used for extrapolation. The tool also reports the integrated RMS phase noise in radians and degrees.

## Features

- Carrier frequency input in Hz / kHz / MHz / GHz
- Editable phase noise table with add/remove rows
- Configurable integration range (default 12 Hz – 1 MHz)
- One-click 10 MHz OCXO example dataset
- 100% client-side: single HTML file, no external dependencies, no data leaves your browser

## Related RF tools

- More RF tools: [BRIDZA RF Component Selector](https://rf.bridza.com/)
- [OCXO / TCXO Parametric Search](https://xiaokeni2.github.io/rf-component-selector/)

## License

MIT
