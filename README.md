
# 📈 Interactive Time Series Analysis App

This Shiny application provides a user-friendly interface for **uploading time series data**, conducting **exploratory data analysis (EDA)**, checking **stationarity**, applying **smoothing techniques**, and fitting **time series models** such as **ARIMA**, **SARIMA**, and **GARCH**.

## 🚀 Features

- 📤 Upload your own CSV file
- 📅 Select **Date** and **Value** columns
- 🔁 Automatically suggest differencing for stationarity
- 📊 Plot Original & Differenced Series
- 🔎 Perform ADF test and examine ACF/PACF
- 📈 Apply Smoothing: Moving Average, Exponential Smoothing, Holt-Winters
- 📦 Fit models based on data characteristics:
  - ARIMA (non-seasonal)
  - SARIMA (seasonal)
  - GARCH (high volatility)
- 🔮 Generate forecasts with visualization
- 📉 Diagnostic checks using Ljung-Box test

## 🛠️ Tech Stack

- **Language**: R
- **Framework**: Shiny
- **Libraries**: 
  - `forecast`
  - `tseries`
  - `ggplot2`
  - `lubridate`
  - `readr`
  - `ggfortify`
  - `TSstudio`
  - `rugarch`

## 📦 Installation

Ensure R and RStudio are installed. Then install the required packages:

```r
install.packages(c("shiny", "forecast", "tseries", "ggplot2", 
                   "lubridate", "readr", "ggfortify", "TSstudio"))
install.packages("rugarch", repos="https://cloud.r-project.org")
```

## ▶️ Run the App

You can run the app locally via RStudio:

```r
library(shiny)
runApp("path_to_app_directory")
```

Alternatively, host it using **shinyapps.io** or your own Shiny Server.

## 📂 File Upload Format

The app expects a CSV file with at least:
- A **Date** column (in `yyyy-mm-dd` format or compatible with `as.Date`)
- A **Value** column (numerical)

Example:

| Date       | Sales |
|------------|-------|
| 2023-01-01 | 100   |
| 2023-02-01 | 120   |

## 🧠 Model Logic

- **Stationarity Check**: ADF Test after differencing
- **Seasonality Detection**: Based on ACF at seasonal lags
- **Model Selection**:
  - **ARIMA**: if stationary and no strong seasonality
  - **SARIMA**: if seasonal patterns detected
  - **GARCH**: if data shows volatility clustering

## 📋 TODO

- [ ] Add seasonal decomposition
- [ ] Allow seasonal adjustment before modeling
- [ ] Export reports as PDF/HTML
- [ ] Enable custom forecast horizon input

## 🤝 Contributing

Pull requests and feedback are welcome! Please open an issue first to discuss major changes.

## 📄 License

MIT License. Feel free to use, modify, and distribute.

## 👤 Author

**[Your Name]**  
_Masters in Statistics | Time Series Enthusiast_  
[LinkedIn](#) | [GitHub](#)
