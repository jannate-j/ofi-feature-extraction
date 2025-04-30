# ofi-feature-extraction

This repository contains my work for the Order Flow Imbalance (OFI) feature extraction task using the provided `first_25000_rows.csv` dataset.

The goal was to implement different OFI features based on limit order book activity. I focused on keeping the code readable and practical, and tried to stay close to the structure described in the task.

- **Best-Level OFI** – computed from depth 0 (top of book), based on adds and cancels.
- **Multi-Level OFI** – includes depths 0 through 5, with a weighting scheme that gives more importance to shallower levels.
- **Integrated OFI** – rolling sum over a 10-tick window using the best-level OFI.
- **Cross-Asset OFI** – this part was skipped because the dataset only included one symbol (AAPL), so there wasn’t any cross-asset data to use.

## File Overview

- `ofi_feature_work.ipynb` – the main notebook with my code and step-by-step feature calculations.
- `README.md` – this file :)


## Notes

- The code is written in a straightforward way — I didn’t try to over-engineer it.
- You can run the notebook in Google Colab; just make sure the CSV file is uploaded and the path is correct.
- I added comments where I thought it would help clarify my thought process.

Thanks for reading. Let me know if you'd like me to explain any part of the logic.
