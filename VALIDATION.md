# Supplied dataset validation

All 16 executable notebook cells completed in order. The existing notebook sequence, inline FRQI functions, original upload/Compare handler, MNIST benchmark, and recovery comparison are retained. No cell errors were recorded.

All 12 attachment files are included under their original names, and each bundled file was verified byte-for-byte against its source and its recorded SHA-256 checksum. No prior sunset, stock scene, or simulated photo is present. The photo-source order follows the supplied attachment order.

Coverage:
- 144 forward photo brightness rows: 12 images × 2 sizes (8, 16) × 3 increases × 2 original methods (controlled multiplicative and global additive).
- 24 photo negative rows: all 12 images at both sizes.
- 12 original-versus-transform galleries, one per supplied photo.
- 144 recovery-quality rows: 12 images × 4 conditions (three increases plus negative) × 3 methods (classical, exact quantum, twice-sampled quantum).
- 48 six-panel recovery figures and matching floating-point array archives.
- The required balanced 20-image actual MNIST study at 4×4/8×8 and the original synthetic checks also completed.

Maximum exact photo MAE for controlled multiplication versus its matching classical target: 1.6794e-06 grayscale levels. Maximum classical-versus-exact recovered pixel difference: 1.9422e-05. No quantum quality advantage is assumed; ideal exact outputs agree within numerical precision, and sampling adds error. The global additive method can wrap and is not expected to match clipped multiplication.

The original Compare handler completed all 12 grid/percentage combinations using the first supplied cave photo. This tests the callback code, not native browser file-picker interaction. Numerical recovery regression checks passed for unclipped reversibility, irreversible clipping, and double-negative recovery. The denied-current-directory regression also passed using a validated project-folder fallback. Folder detection checks this dataset's identity, preventing a silent fallback to a previous image collection.

The 12 inputs contain both dark and mixed/bright scenes; individual notes identify glare, haze, source softness, and possible highlight clipping. All are retained, none is artificially blurred or darkened, and only +10%, +25%, +50% brightness increases are introduced. No paired normal-light reference exists, and no missing ground truth is manufactured.

Execution used Python 3.13, Qiskit 2.5.1, and the existing local dependencies with in-process IPython rich-output capture. Live browser interaction, a network-bound Jupyter server, hardware execution, and fresh dependency installation were not tested. Simulation resolution, exact state access, and ideal shot sampling limitations remain documented.
