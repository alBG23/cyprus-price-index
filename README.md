# Cyprus Price Index

Open monthly data on how much online prices for the **same product** differ between shops in Cyprus.
Made by [Pricely](https://pricely.cy), a free price-comparison site that checks about 180 Cyprus online shops every night.

The full index, with explanations in English, Greek and Russian, is at **[pricely.cy/cyprus-price-index](https://pricely.cy/cyprus-price-index)**.

## October 2026 so far (figures of 21 Oct)

- **402,103** products in stock across **186** Cyprus online shops.
- **31,727** of them are sold by 2 or more shops, so their prices can be compared directly.
- For those products, the most expensive shop charges on average **19.9% more** than the cheapest one.
- The gap is widest in **Electronics (26.6% on average)** and narrowest in **Baby & Toys (10.4%)**.

| Category | Products at 2+ shops | Average gap | Median gap | Cheapest shop most often |
|---|---:|---:|---:|---|
| Beauty | 14,771 | 20.5% | 13.3% | MyPharmacy |
| Electronics | 7,076 | 26.6% | 15.0% | MSystems |
| Baby & Toys | 4,891 | 10.4% | 0.2% | Toys-shop |
| Home Appliances | 3,355 | 20.0% | 12.0% | Kotsovolos |
| Pet | 796 | 12.6% | 9.7% | Pets For All |
| Home & Furniture | 537 | 16.9% | 8.5% | Toys-shop |
| Sport | 296 | 11.3% | 1.1% | Runner Store |

## Files

- [`data/latest.csv`](data/latest.csv): the most recent month.
- `data/cyprus-price-index-YYYY-MM.csv`: one file per month.

| Column | Meaning |
|---|---|
| `month` | Year and month, e.g. `2026-10` |
| `category` | Product category group |
| `products_in_stock` | Products in stock at at least one shop |
| `products_at_2plus_shops` | Products in stock at 2 or more shops (the ones compared) |
| `avg_gap_cheapest_to_most_expensive_pct` | Average difference between the most expensive and the cheapest shop, as % of the cheapest price |
| `median_gap_pct` | The same, median (half the products differ by less than this) |
| `cheapest_shop_most_often` | The shop that has the lowest price most often in this category |
| `cheapest_shop_share_pct` | Of that shop's compared products, the share where it is the cheapest |

## How it is made

- Prices come from each shop's own public website, read every night, in euro as the shop shows them.
- A product is matched across shops by its barcode (EAN) or exact model code first, and only then by name.
- Each month's file shows the figures for the last day of that month (the current month is refreshed daily on pricely.cy).
- Categories with fewer than 50 compared products are left out.
- Delivery costs are not included. Stock changes often: the shop's own site has the final word.

## Use it freely

The data is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You can use it in articles, research, apps or AI tools, including commercially, as long as you credit:

> Source: Cyprus Price Index by Pricely (pricely.cy)

Questions or a story idea? Use the contact form at [pricely.cy/contact](https://pricely.cy/contact).
