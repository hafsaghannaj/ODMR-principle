# Physical Parameters

All figures in this repository use synthetic (illustrative) models with physically motivated
parameters drawn from the NV-center literature. No experimental data is plotted.

---

## Figure 3 — Zeeman Splitting

ODMR spectrum modeled as a sum of two Lorentzian dips centered at D ± gamma_e * B.

| Parameter | Value | Unit | Source |
|---|---|---|---|
| Zero-field splitting (D) | 2.870 | GHz | Doherty et al. (2013), Table 1 |
| Electron gyromagnetic ratio (gamma_e) | 28.025 | GHz/T | CODATA 2018 |
| Applied magnetic fields (B) | 0, 3, 5 | mT | Chosen for visual clarity |
| Dip contrast | 3.5% | — | Typical experimental range: 1–30% |
| Lorentzian FWHM linewidth | 10 | MHz | Typical for ensemble NV (5–30 MHz) |
| Frequency axis | 2.80–2.94 | GHz | Centered on D |
| Frequency points | 1200 | — | Sufficient for smooth rendering |
| Baseline fluorescence | 1.0 | a.u. | Normalized |

**Model:** `y(f) = baseline - contrast * sum[ gamma^2 / ((f - c_i)^2 + gamma^2) ]`
where `gamma = FWHM / 2` and `c_i = D ± gamma_e * B`.

**Validation:** At B = 5 mT, expected splitting is 2 * 28.025 * 0.005 = 0.280 GHz,
giving dips at ~2.730 and ~3.010 GHz. This is consistent with the known
~2.8 MHz/G (= 28 GHz/T) NV ground-state splitting factor.

---

## Figure 6 — Temperature Shift

Linear model of zero-field splitting D as a function of temperature.

| Parameter | Value | Unit | Source |
|---|---|---|---|
| D at reference temperature | 2.870 | GHz | Doherty et al. (2013) |
| Reference temperature (T0) | 300 | K | Room temperature |
| Temperature coefficient (dD/dT) | -74.2 | kHz/K | Acosta et al. (2010), Phys. Rev. Lett. 104, 070801 |
| Temperature range | 270–330 | K | Near room temperature |
| Temperature points | 200 | — | Sufficient for smooth rendering |

**Model:** `D(T) = D0 + (dD/dT) * (T - T0)`

**Validation:** The coefficient dD/dT = -74.2 kHz/K is the widely cited value from
Acosta et al. (2010). Over the plotted range (270–330 K), D shifts by approximately
±2.2 MHz from its room-temperature value of 2.870 GHz, consistent with published data.

---

## References

1. Doherty, M.W. et al. "The nitrogen-vacancy colour centre in diamond."
   *Physics Reports* **528**, 1–45 (2013). doi:10.1016/j.physrep.2013.02.001

2. Acosta, V.M. et al. "Temperature Dependence of the Nitrogen-Vacancy Magnetic Resonance in Diamond."
   *Phys. Rev. Lett.* **104**, 070801 (2010). doi:10.1103/PhysRevLett.104.070801

3. CODATA 2018: Electron gyromagnetic ratio, NIST.
   https://physics.nist.gov/cgi-bin/cuu/Value?gammae
