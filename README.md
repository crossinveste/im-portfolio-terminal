# Investment Management — Live Portfolio & Attribution Frame

Live Link: **https://crossinveste.github.io/im-portfolio-terminal/**

## How Live Updates Work
1. **Viewers (Zero Setup):** Anyone opening the link sees the latest locked portfolio snapshot and automatically receives live updates on screen within ~5–10 seconds whenever a new Feeder Excel workbook is uploaded (via zero-quota GitHub `ETag` polling).
2. **Confidentiality by Design:** When `Portfolio_Bloomberg_Feeder_Optimized.xlsx` is dropped into **Upload & Publish Live**, the `.xlsx` file is parsed 100% locally in the uploader's browser and stripped of all dollar `MV` and `AUM` values before committing only sanitized percentage weights and returns to `data/snapshot.json`.

## One-Time Publisher Setup (30 Seconds)
To publish live updates from your browser when dropping `Portfolio_Bloomberg_Feeder_Optimized.xlsx`:
1. Go to [GitHub Fine-Grained Personal Access Tokens](https://github.com/settings/personal-access-tokens/new).
2. Under **Repository access**, select **Only select repositories** -> `im-portfolio-terminal` (and set **Expiration** up to 1 year, or use a dedicated account token).
3. Under **Repository permissions**, set **Contents** to **Read and write** and click **Generate token**.
4. Click **Upload & Publish Live** on the dashboard, paste the token once (saved only in your browser's `localStorage`), and drop your saved `.xlsx` file.
