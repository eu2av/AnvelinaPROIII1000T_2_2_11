    2026 May 05 - (eu2av) Firmware Update: PureSignal Feedback Path Optimization
    Implemented adaptive scaling in the PureSignal feedback loop (temp_DACD). By dynamically shifting the bit-window
    extraction, the feedback signal maintains full 16-bit resolution even at low output power (1–5 W). Result:
    faster convergence, stable predistortion correction across all power levels, improved IMD3 suppression on weak signals.
    DSP Chain Optimization:
    RX: Implemented TPDF Dither before CIC decimation. Result: Elimination of quantization noise structure ("grid" on panadapter), improved Dynamic Range (+6-9 dB).
    TX/NCO: Added Phase Dither to CORDIC phase accumulator. Result: Significant reduction of spurious harmonics (spurs), improved SFDR (+10-15 dB).
    Filters: Changed FIR truncation to "round-to-nearest" logic. Result: Eliminated DC offset peak at center frequency, improved calculation accuracy.
    PureSignal: Added adaptive scaling for the feedback path to ensure stable convergence at low output power levels. 


