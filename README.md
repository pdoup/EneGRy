# EneGRy
Time-series data combining multiple sources to explain the broader Greek energy market

This repository contains a **curated time-series dataset** that combines **daily** data from the energy sector, weather data, and market data for Greece. The dataset spans from December 1st, 2020, to August 18th, 2023, and includes information on energy-related futures contracts, day-ahead energy market prices, and more.

The dataset is set to serve as a valuable resource for data analysts and scientists interested in conducting exploratory data analysis or predictive tasks. For example, the dataset can be used to predict tomorrow's energy demands or wholesale prices.

One of the key features of this dataset is that it contains data from renewable energy sources. This, along with the comprehensive daily weather condition data, makes it an excellent resource for gaining insights into the renewable energy market in Greece.

In addition to the information mentioned earlier, this dataset also incorporates information about global markets. This means that it has the potential to uncover latent relationships between the energy sector, weather data, and market data in Greece and global markets. By analyzing this dataset, data analysts and scientists can gain a deeper understanding of how global market trends and events impact the energy sector in Greece. This makes the dataset an even more valuable resource for conducting exploratory data analysis or predictive tasks.

## Potential Uses

- **Exploratory Data Analysis**: The dataset can be used to explore trends and patterns in the energy sector, weather data, and market data for Greece.
- **Predictive Tasks**: The dataset can be used to develop predictive models for forecasting energy demands or wholesale prices.
- **Renewable Energy Market Insights**: The dataset contains data from renewable energy sources, making it a valuable resource for gaining insights into the renewable energy market in Greece.
- **Global Market Insights**: The dataset incorporates information about global markets, allowing analysts to uncover latent relationships between the energy sector in Greece and global markets.

## Data Sources and APIs

The data in this dataset was retrieved from multiple sources and APIs. These sources include:

1. [data.gov.gr](https://data.gov.gr/)
2. [admie.gr](https://www.admie.gr/)
3. [IBM Environmental Intelligence Suite APIs](https://www.ibm.com/products/environmental-intelligence-suite/apis)
4. [tradingeconomics.com](https://tradingeconomics.com/)
5. [transparency.entsoe.eu](https://transparency.entsoe.eu/)

This curated dataset is a valuable resource for anyone interested in conducting analysis on the energy sector, weather data, and market data for Greece. It is available for download on this GitHub repository.

## Description

<details>
  <summary>Click to expand</summary>
  
  |Feature|Type|Unit|Description|
| :------------ | :------------ | :------------ | :------------ |
|temp_min|int|`°C`|Minimum recorded temperature ; station `LGAV`, Spata, Attica, Greece|
|temp_max|int|`°C`|Maximum recorded temperature ; station `LGAV`, Spata, Attica, Greece|
|temp_avg|float|`°C`|Daily average temperature ; station `LGAV`, Spata, Attica, Greece|
|wx_phrase_most_freq|string|-|Most prominent expected weather conditions throughout that day (e.g., `Fair`, `Partly Cloudy`, `Light Rain`)|
|dewPt_min|int|`°C`|Minimum temperature at dew-point ; station `LGAV`, Spata, Attica, Greece|
|dewPt_max|int|`°C`|Maximum temperature at dew-point ; station `LGAV`, Spata, Attica, Greece|
|dewPt_avg|float|`°C`|Daily average temperature at dew-point ; station `LGAV`, Spata, Attica, Greece|
|heat_index_min|int|`°C`|Minimum recorded HI ; station `LGAV`, Spata, Attica, Greece. (HI: human-perceived equivalent temperature)|
|heat_index_max|int|`°C`|Maximum recorded HI ; station `LGAV`, Spata, Attica, Greece.|
|heat_index_avg|float|`°C`|Daily average HI ; station `LGAV`, Spata, Attica, Greece.|
|rh_min|int|`%`|Minimum relative-humidity ; station `LGAV`, Spata, Attica, Greece. Ranges from `0` to `100`|
|rh_max|int|`%`|Maximum relative-humidity ; station `LGAV`, Spata, Attica, Greece. Ranges from `0` to `100`|
|rh_avg|float|`%)`|Daily average relative-humidity ; station `LGAV`, Spata, Attica, Greece. Ranges from `0` to `100`|
|pressure_avg|float|`hPa/mbar`|Daily average atmospheric pressure ; station `LGAV`, Spata, Attica, Greece|
|vis_avg|int|`km (kilometer)`|Daily average visibility ; station `LGAV`, Spata, Attica, Greece|
|wdir_avg|int|`degrees (°)`|Daily average wind direction; station `LGAV`, Spata, Attica, Greece|
|wdir_cardinal_most_freq|string|-|Daily average secondary intercardinal directions (e.g., `SSW`, `VAR`, `NNW`); station `LGAV`, Spata, Attica, Greece|
|gust_max|int|`km/h`|Maximum recorded wind gusts; station `LGAV`, Spata, Attica, Greece|
|wspd_min|int|`km/h`|Minimum wind speed ; station `LGAV`, Spata, Attica, Greece|
|wspd_max|int|`km/h`|Maximum wind speed ; station `LGAV`, Spata, Attica, Greece|
|wspd_avg|float|`km/h`|Daily average wind speed ; station `LGAV`, Spata, Attica, Greece|
|uv_desc_least_freq|string|-|Least prominent ultraviolet-index for the day (e.g., `Low`, `Moderate`) ; station `LGAV`, Spata, Attica, Greece|
|uv_desc_most_freq|string|-|Most prominent ultraviolet-index for the day (e.g., `Low`, `Moderate`) ; station `LGAV`, Spata, Attica, Greece|
|uv_index_min|int|`scale (0-11+)`|Lowest recorded UV index; station `LGAV`, Spata, Attica, Greece|
|uv_index_max|int|`scale (0-11+)`|Highest recorded UV index; station `LGAV`, Spata, Attica, Greece|
|clds_most_freq|string|-|Most observed sky cloud coverage; station `LGAV`, Spata, Attica, Greece. ![More info](https://github.com/pdoup/EneGRy/blob/main/images/clouds_exp.png)|
|gas_load|int|`MWh`|Total gas load on the energy grid `GR`|
|wind_power_load|int|`MWh`|Load attributed to wind power generators `GR`|
|renewable_energy_load|int|`MWh`|Load attributed to renewable energy sources available on the power grid `GR`|
|net_imports|int|`MWh`|Total (`Imported` - `Exported`) energy balance `GR`|
|coal_load|int|`MWh`|Load attributed to traditional coal-fired plants available on the power grid `GR`|
|natural_gas_load|int|`MWh`|Total natural gas load on the energy grid `GR`|
|hydropower_load|int|`MWh`|Load on the energy grid from hydroelectric sources `GR`|
|gross_energy_load|int|`MWh`|Represents the quantity of energy necessary to satisfy domestic energy demands `GR`|
|renewable_energy_production|int|`MWh`|Total power produced by renewable energy sources `GR`|
|day_ahead_market_avg_clearing_price|float|`EUR / MWh`|For every market time  unit (typically `1H`) the day-ahead prices in each bidding zone (Currency/MWh) `GR`. The hourly clearing prices are aggregated to a daily average, meant to represent the daily mean wholesale price|
|wind_energy_index|float|`USD`|Tracks the performance of publicly traded companies in the wind energy sector as well as those businesses that do not produce energy but make most of their revenues by providing goods and services to the wind energy industry.|
|wind_energy_index_pct_change|float|`%`|Daily shift in the wind index expressed as a percentage.|
|wind_energy_index_change|float|-|Daily shift in the wind index expressed as the numeric difference (`current_index` - `previous_index`).|
|solar_energy_index|float|`USD`|Tracks the performance of publicly traded companies in the solar energy sector as well as those businesses that do not produce energy but make most of their revenues by providing goods and services to the solar energy industry.|
|solar_energy_index_pct_change|float|`%`|Daily shift in the solar index expressed as a percentage.|
|solar_energy_index_change|float|-|Daily shift in the solar index expressed as the numeric difference (`current_index` - `previous_index`).|
|heating_oil_futures_US|float|`USD`|Heating oil, also known as No. 2 fuel oil futures.|
|heating_oil_futures_US_pct_change|float|`%`|Daily shift in the heating oil futures contracts expressed as a percentage.|
|heating_oil_futures_US_change|float|-|Daily shift in the heating oil futures contracts prices expressed as the numeric difference (`current` - `previous`).|
|carbon_permits_EU|float|`EUR`|Sourced from the European Union Emissions Trading System (EU ETS). Allowances for carbon emissions are first allocated considering EU directives for the maximum amount of greenhouse gases that can be emitted (can be traded).|
|carbon_permits_EU_pct_change|float|`%`|Daily shift in the allowances price for carbon emissions expressed as a percentage.|
|carbon_permits_EU_change|float|-|Daily shift in the allowances price for carbon emissions expressed as the numeric difference (`current` - `previous`).|
|coal_futures|float|`USD`|Newcastle coal futures. The standard GC Newcastle contact listed on Intercontinental Exchange (ICE) weights 1,000 metric tonnes.|
|coal_futures_pct_change|float|`%`|Daily shift in the coal futures contracts expressed as a percentage.|
|coal_futures_change|float|-|Daily shift in the coal futures contracts prices expressed as the numeric difference (`current` - `previous`).|
|natural_gas_eu_dutch_ttf_prices|float|`EUR/MWh`|Dutch TTF Gas. European benchmark for gas prices stipulating physical delivery as part of the agreement.|
|natural_gas_eu_dutch_ttf_prices_pct_change|float|`%`|Daily shift in the Dutch TTF Gas contracts expressed as a percentage.|
|natural_gas_eu_dutch_ttf_prices_change|float|-|Daily shift in the Dutch TTF Gas contracts prices expressed as the numeric difference (`current` - `previous`).|
|wti_crude_oil_futures|float|`USD/Bbl`|West Texas Intermediate (WTI) benchmark for US crude.|
|wti_crude_oil_futures_pct_change|float|`%`|Daily shift in the WTI futures contracts expressed as a percentage.|
|wti_crude_oil_futures_change|float|-|Daily shift in the WTI futures contracts expressed as the numeric difference (`current` - `previous`).|  
</details>

## Citing this Dataset

If you use this dataset in your research or analysis, please cite it using the following entry:

```
@misc{EneGRy,
  title={EneGRy},
  author={Panagiotis Doupidis},
  year={2023},
  publisher={GitHub},
  howpublished={\url{[EnergyGR2020_2023](https://github.com/pdoup/EneGRy)}},
}
```

## License

The data can be used as is without any warranty. Taking into account the size and factual nature of the data along with the sources, this falls under the Public Domain Dedication and License (PDDL).
