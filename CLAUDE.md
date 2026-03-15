# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website that visualizes Shanghai vehicle license plate (沪牌) auction price trends from 2002 to present. The site displays historical data including:
- Auction date
- License plate supply quantity (投放数量)
- Minimum winning bid (最低成交价)
- Average winning bid (平均成交价)
- Number of bidders (投标人数)

## Architecture

Single-page static website using:
- **ECharts 5** for interactive data visualization (loaded from jsdelivr CDN)
- Vanilla JavaScript for chart rendering
- Embedded historical auction data (no external API)

## Key Files

- `index.html` - Main page containing all HTML, CSS, JavaScript, and embedded data
- `README.md` - Project documentation with live demo link

## Data Source

Data is sourced from 上海国拍 (https://www.alltobid.com/contents/16/71.html) and manually updated in the `data` array within `index.html`. The data format is:
```javascript
["YYYY.M", supply, minPrice, avgPrice, null, bidders]
```

## Common Tasks

- **Update data**: Add new monthly data entries to the `data` array in `index.html`, following the existing format
- **Deploy**: Push changes to master branch - GitHub Pages automatically deploys from the `master` branch at https://cygra.github.io/shanghai-vehicle-license-price-trend/
