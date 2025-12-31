# DeductibleData Test Datasets

Test data files for [deductible-tic](https://github.com/DeductibleData-co/deductible-tic) price transparency processing.

## Table of Contents File

**URL**: `https://raw.githubusercontent.com/DeductibleData-co/datasets/main/2025-01-01_table-of-contents-mixed-types.json`

## In-Network Files

| File | Source | Billing Types |
|------|--------|---------------|
| `in-network-rates-mixed-types.json` | DeductibleData | CPT, MS-DRG, HCPCS, RC |
| CMS multiple-plans-sample.json | CMSgov | CPT |
| CMS bundle-single-plan-sample.json | CMSgov | ICD |
| CMS capitation-single-plan-sample.json | CMSgov | CPT |
| CMS fee-for-service-single-plan-sample.json | CMSgov | CPT |
| CMS no-npi.json | CMSgov | CPT |

## Mixed Types Test File

Our `in-network-rates-mixed-types.json` contains:

| Billing Type | Codes | Description |
|--------------|-------|-------------|
| CPT | 27447, 27130 | Knee/hip arthroplasty |
| MS-DRG | 470, 469 | Major joint replacement |
| HCPCS | G0438 | Annual wellness visit |
| RC | 0120 | Room and board |

## Usage

Configure `test_payer` in `main.py`:
```python
urls.append(
    "https://raw.githubusercontent.com/DeductibleData-co/datasets/main/2025-01-01_table-of-contents-mixed-types.json"
)
```
