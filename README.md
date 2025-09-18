
# Hippocampus Secure Demo - README

This folder contains a secure demo for a simulated neural implant communication stack.

Files:
- hippocampus.py : Secure demo server (requires `cryptography` Python package).
- implant_sim.py : Simulated implant client.
- docker-compose.yml : Example composition to run both in containers.
- Hardware_BOM.csv : Recommended hardware components (vendor-neutral).
- Threat_Model_Neural_Implant.pdf : Threat model document.
- Security_Requirements_and_Test_Plan.pdf : Security requirements and test plan.

## Running locally (recommended for development / testing only)

1. Create a Python virtual environment and install dependencies:
```bash
python3 -m venv venv
source venv/bin/activate
pip install cryptography
```

2. Run the server:
```bash
python3 /mnt/data/hippocampus_secure_demo/hippocampus.py
```

3. In another terminal, run the simulated implant:
```bash
python3 /mnt/data/hippocampus_secure_demo/implant_sim.py
```

The demo stores keys and registry under `/mnt/data/hippocampus_secure_demo/keys`.

## Running with docker-compose (optional)
Ensure `docker` and `docker-compose` are installed. From the folder that contains `hippocampus_secure_demo` and this `docker-compose.yml` file, run:

```bash
docker compose up
```

## Important Safety & Legal Notes
- This demo is for development, simulation, and educational purposes only. **Do NOT** use this code with any real implanted hardware or in clinical contexts without appropriate regulatory approvals, clinical oversight, and medical device engineering controls.
- Real-world implant systems require certified hardware secure elements, HSMs for signing, audited cryptographic implementations, and must follow medical device regulations (FDA, MDR, Health Canada, etc.).
- The maintainers are not responsible for misuse of this code.

