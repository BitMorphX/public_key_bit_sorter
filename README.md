<p align="center">
  <img src="assets/banner.png" alt="python public_key_bit_sorter banner" width="100%" />
</p>

# Public Key Bit Sorter

This tool sorts ECDSA uncompressed public keys (format `04...`, 130 characters) into separate files based on their effective bit lengths.  
Four different bit-counting strategies are supported to analyze the entropy or structure of public keys.

---

## 📊 Bit-Counting Methods Comparison

| Method            | Description                                                    | Usefulness                                                  |
|-------------------|----------------------------------------------------------------|-------------------------------------------------------------|
| **1. Classic**     | Total bits = HEX length × 4                                    | Basic grouping, includes all leading zeros                 |
| **2. Dynamic**     | Sum of X and Y binary lengths, excluding leading zeros         | Measures real entropy, great for weak key detection        |
| **3. Legacy**      | MAX HEX length of X or Y (no leading zeros), × 4              | Fast approximation, good for dominant coordinate detection |
| **4. Binary-Max**  | MAX binary bit length of X or Y, no leading zeros             | Most accurate entropy estimate                             |

---

## ⚙️ Features

- 4 bit-counting strategies  
- Multiprocessing (parallel key sorting)  
- `tqdm` live progress bar  
- Grouped outputs saved in `output/`  
- Works on Linux, macOS, Windows  

---

## 🧪 Requirements

```bash
pip install tqdm
```

Python 3.8 or newer is recommended.

---

## 📂 Usage

```bash
python public_key_bit_sorter.py
```

Follow interactive prompts:

1. Input file name (default: `publickeys.txt`)  
2. Choose bit-counting method (1–4)  
3. Set number of CPU threads  

Output files will be saved like:

```
output/publickeys_256bit.txt  
output/publickeys_253bit.txt  
...
```

---

## 📁 File Overview

- `public_key_bit_sorter.py` – Main script  
- `public_key_bit_sorter.bat` – Windows launcher  
- `publickeys.txt` – Sample input file with public keys  
- `output/` – Generated output directory with grouped keys  
- `requirements.txt` – Dependencies  
- `README.md` – This documentation  
- `LICENSE` – Apache 2.0 License  
- `NOTICE` – Legal notice and attribution  
- `ETHICS.md` – Responsible use guidelines  
- `RELEASE_v1.0.0.md` – First release notes  
- `RELEASE_v2.0.0.md` – Latest updates  
- `.vscode/` – Editor configuration  
  - `settings.json`  
  - `launch.json`  
  - `tasks.json`  
  - `extensions.json`  
- `assets/` – Contains banner image  

---

## 📦 Project Structure

```text
├── assets/
│   └── banner.png
├── .vscode/
│   ├── settings.json
│   ├── launch.json
│   ├── tasks.json
│   └── extensions.json
├── public_key_bit_sorter.py
├── public_key_bit_sorter.bat
├── publickeys.txt
├── output/
│   └── (generated result files after script runs)
├── requirements.txt
├── README.md
├── LICENSE
├── NOTICE
├── ETHICS.md
├── RELEASE_v1.0.0.md
└── RELEASE_v2.0.0.md
```

---

## ⚠️ Disclaimer

This software is provided strictly for **educational, analytical, and research purposes only**.  
It does **not** include or generate private keys linked to real cryptocurrency wallets.  
The author **does not promote** unethical behavior or unauthorized access to cryptographic systems.  
Use of this tool is the sole responsibility of the user.

---

## ⚖️ Ethical Use

This tool is created strictly for **research and educational purposes**.  
See [ETHICS.md](./ETHICS.md) for full ethical guidelines.

---

## 📜 License

Licensed under the [Apache 2.0 License](./LICENSE).

---

## 📣 Notice

See [NOTICE](./NOTICE) for attribution, DMCA protection, and reuse conditions.

---

## 🍱 Support

★ **Bitcoin (BTC)**  
`1MorphXyhHpgmYSfvwUpWojphfLTjrNXc7`

★ **Monero (XMR)**  
`86VAmEogaZF5WDwR3SKtEC6HSEUh6JPA1gVGcny68XmSJ1pYBbGLmdzEB1ZzGModLBXkG3WbRv12mSKv4KnD8i9w7VTg2uu`

★ **Dash (DASH)**  
`XtNuNfgaEXFKhtfxAKuDkdysxUqaZm7TDX`

**We also value early privacy coins such as:**  
★ **Bytecoin (BCN)**  
`bcnZNMyrDrweQgoKH6zpWaE2kW1VZRsX3aDEqnxBVEQfjNnPK6vvNMNRPA4S7YxfhsStzyJeP16woK6G7cRBydZm2TvLFB2eeR`

🙏 *Thank you for supporting independent research and ethical technology.*

---

## 👤 Author & Contact

🔗 GitHub: https://github.com/BitMorphX  
✉️ Email: BitMorphX@proton.me  
💬 Telegram: https://t.me/BitMorphX

> _“I morph bits, not to break, but to understand.”_  
> — **BitMorphX**

---

© BitMorphX – All rights reserved.
