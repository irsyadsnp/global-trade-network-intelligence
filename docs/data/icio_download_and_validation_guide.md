# Download and Validation Guide — OECD ICIO 2026 Regular

**Purpose:** Download the official OECD ICIO 2026 Regular documentation and one sample data block, then validate the files before acquiring the remaining periods.  
**Guide status:** Instructions only. No download is represented as completed.  
**Official source:** https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html

## 0. Important dataset distinction

This project currently targets **2026 Regular ICIO**, not Extended ICIO.

The OECD landing page states that Regular ICIO covers 95 economies (83 individual countries and 12 regional aggregates). Extended ICIO covers the same broad set but splits China and Mexico to account for firm heterogeneity.

Do not download the Extended files for this initial workflow. Do not mix Regular and Extended data.

Also distinguish:
- Conventional ICIO tables are current-price tables.
- OECD's Previous Year's Prices (PYP) ICIO is a separate product intended for volume analysis. The 2026 PYP release is described separately and has different coverage (80 economies plus a Rest-of-World aggregate and 50 industries). Do not substitute PYP files for the Regular ICIO files.

The OECD ICIO landing page lists the 2026 Regular groups: 1995–1999, 2000–2004, 2005–2009, 2010–2014, 2015–2019, and 2020–2024. It also lists an Annex and ReadMe.

## 1. Prepare a local download folder

Create a folder outside the GitHub repository so raw source files are not accidentally committed.

Suggested folder name:

`global-trade-network-intelligence/source_downloads/icio_2026_regular/`

Inside it, create:
- `documentation/`
- `sample/`

Keep the original downloaded filenames. Do not rename or edit source files.

## 2. Open the official OECD page

1. Open: https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html
2. Scroll to the heading **2026 release (regular ICIO)**.
3. Confirm that you are in the Regular section, not the Extended section below it.
4. Locate the links named **Annex**, **ReadMe**, and the six period groups.
5. Do not use the 2025 or 2023 release links further down the page.

## 3. Download the Annex

1. Click **Annex** directly under **2026 release (regular ICIO)**.
2. If the browser opens a document preview, use its download icon or the browser's Save option.
3. Save it into the local `documentation/` folder.
4. Keep its original extension and filename.
5. Open it and inspect the sheets/pages that describe economy codes, industry classification, table structure, or metadata.
6. Do not infer the file's contents from its filename alone.

Record the exact filename and file type in the acquisition log.

## 4. Download the ReadMe

1. Return to the same OECD page.
2. Under **2026 release (regular ICIO)**, click **ReadMe**.
3. Save it into the same `documentation/` folder.
4. Open it in the appropriate application:
   - XLSX: LibreOffice Calc or Excel.
   - PDF: a PDF reader.
   - TXT/CSV: a text editor or spreadsheet application.
5. Inspect and record:
   - economy identifiers and labels;
   - industry codes and labels;
   - table/matrix names;
   - row and column layout;
   - units, currency, and valuation basis;
   - treatment of intermediate use and final demand;
   - any notes about revisions, estimates, or exceptions.

If a detail is not stated, record it as **not specified in the ReadMe** rather than guessing.

## 5. Download one sample period only

For the first technical test, use **1995–1999** from the 2026 Regular section.

1. Return to the OECD page.
2. Confirm the heading still says **2026 release (regular ICIO)**.
3. Click **1995–1999** within that section.
4. If a download starts, wait for it to complete.
5. If a browser preview opens, use the download control.
6. Save the original file into `sample/`.
7. Do not download all six groups yet.

Why start with one block: it lets us test the file format, archive integrity, data layout, and software compatibility before spending time and storage on the complete time series.

## 6. Check the downloaded files

### Visual check

For each downloaded file:
- Confirm the file size is not zero.
- Confirm the browser shows a completed download.
- Confirm the extension is plausible for the actual file (for example, ZIP, CSV, XLSX, or another format).
- If the sample is an archive, open it with the system archive manager and check that it lists contents without an error.
- Do not modify files inside the archive.

A file extension alone does not prove that a file is valid.

### Optional checksum on Linux

Open a terminal in the folder containing the downloaded file and run:

```bash
sha256sum "EXACT_FILENAME"
```

Replace `EXACT_FILENAME` with the actual filename, including its extension. Save the full SHA-256 output in the acquisition log. If you do not want to use a terminal, leave the checksum field pending; do not invent one.

## 7. What to send back for review

Upload these three items in the ChatGPT conversation:
1. The downloaded Annex.
2. The downloaded ReadMe.
3. The one 1995–1999 sample archive (or the exact downloaded sample file).

If the sample archive is too large to upload, send:
- the exact filename;
- file size;
- file extension;
- a screenshot of the archive contents;
- the Annex and ReadMe.

Do not upload credentials or personal files. Do not put raw ICIO data into the public GitHub repository at this stage.

## 8. What will be checked after upload

The project audit will verify:

1. Whether the files correspond to the 2026 Regular release.
2. Whether the sample archive opens and passes integrity checks.
3. Exact economy count and identifiers, including regional aggregates and Rest of the World treatment.
4. Exact industry count, codes, and labels.
5. Table names, dimensions, and row/column conventions.
6. Units, currency, and valuation basis.
7. Missing values, zero values, totals, and accounting consistency where testable.
8. Whether the 1995–1999 block is compatible with the documented schema.
9. Any license, attribution, third-party, or redistribution restrictions stated in the documentation.

Only after this review should the project decide whether to download the remaining five groups.

## 9. Acquisition log template

Record the following in `docs/data/acquisition_log.md` after files have actually been downloaded:

| Field | Value |
|---|---|
| Dataset | OECD ICIO 2026 Regular |
| Official page | https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html |
| Access date | YYYY-MM-DD |
| Annex filename | Pending |
| ReadMe filename | Pending |
| Sample group | 1995–1999 |
| Sample filename | Pending |
| Sample size | Pending |
| SHA-256 | Pending |
| Archive integrity | Pending |
| Dataset-specific reuse notes | Pending |

Do not fill pending fields until the corresponding file has been inspected.

## 10. Full acquisition after sample validation

After the sample passes:
1. Confirm the remaining period groups and their exact files.
2. Download each Regular ICIO block.
3. Keep each original file unchanged.
4. Record filename, size, access date, and SHA-256 for every file.
5. Keep raw files outside Git unless the OECD terms and any third-party restrictions clearly permit redistribution.
6. Build reproducible scripts to read and transform the data only after the file schema is confirmed.

## 11. Troubleshooting

- **Click opens a preview instead of downloading:** use the download icon or browser Save option.
- **Download fails:** retry once; if it continues, record the error and use the OECD contact listed on the page.
- **Archive cannot be opened:** do not extract or rename it repeatedly. Re-download and compare file size/checksum if possible.
- **File extension looks unfamiliar:** do not assume it is CSV or ZIP. Keep it unchanged and inspect the actual file type.
- **Annex/ReadMe link is inaccessible:** capture the exact error or screenshot. Do not use old-release documentation as a substitute without recording the mismatch.
- **RData is needed:** the OECD page says RData files can be requested from ICIO-TiVA.Contact@oecd.org. Request the 2026 Regular version explicitly and ask for its schema/read instructions.

## 12. Official references

- OECD, Inter-Country Input-Output tables: https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html
- OECD, Global value chain data across trade, multinationals and services (separate PYP ICIO product): https://www.oecd.org/en/data/datasets/global-value-chain-data-across-trade-multinationals-and-services.html
- OECD, Trends in Global Value Chains (2026): https://www.oecd.org/en/publications/trends-in-global-value-chains_8217c2ff-en.html

**Stop point:** do not proceed to full acquisition or analysis until Annex, ReadMe, and one sample file have been inspected.
