# react-tradingview-widget-ta
React component for rendering the [TradingView Advanced Real-Time Chart Technical Analysis Widget](https://www.tradingview.com/widget/advanced-chart/).

## Install
`yarn add react-tradingview-widget-ta`
or
`npm install --save react-tradingview-widget-ta`

## Usage
### Basic example
```javascript
import TradingViewWidget from 'react-tradingview-widget-ta';

const App = () => (
  <TradingViewWidget symbol="NASDAQ:AAPL" />
);
```

All given props are passed on to the widget config. See [this page](https://www.tradingview.com/widget/advanced-chart/) for the TradingView Advanced Real-Time Chart API.

### Advanced example
```javascript
import TradingViewWidget, { Themes } from 'react-tradingview-widget';

const App = () => (
  <TradingViewWidget
    symbol="NASDAQ:AAPL"
    theme={Themes.DARK}
    locale="fr"
    autosize
  />
);
```

## Constants and API differences
react-tradingview-widget exports constants for the following things:
- Interval types: `IntervalTypes.D` and `IntervalTypes.W`
- Themes: `Themes.LIGHT` and `Themes.DARK`
- BarStyles:
  - `BarStyles.BARS`
  - `BarStyles.CANDLES`
  - `BarStyles.HOLLOW_CANDLES`
  - `BarStyles.HEIKIN_ASHI`
  - `BarStyles.LINE`
  - `BarStyles.AREA`
  - `BarStyles.RENKO`
  - `BarStyles.LINE_BREAK`
  - `BarStyles.KAGI`
  - `BarStyles.POINT_AND_FIGURE`

You don't have to use these constants.

react-tradingview-widget also makes it possible to use numbers for `interval`, `popup_width` and `popup_height` instead of strings, but this is not required.
