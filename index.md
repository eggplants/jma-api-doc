# 気象庁API

## エンドポイント種

- https://www.jma.go.jp/bosai/amedas
  - [amedas](amedas)
- https://www.jma.go.jp/bosai/common
  - [common](common)
- https://www.jma.go.jp/bosai/forecast
  - [forecast](forecast)
- https://www.jma.go.jp/bosai/himawari
  - [himawari](himawari)

## コンテンツ種別一覧(APIは網羅されていない)

- <http://www.jma.go.jp/bosai/common/const/contents.json>

### `.groups`

```json
[
  {
    "type": "bousai",
    "name": "防災",
    "enName": "BOSAI",
    "priority": 0
  },
  {
    "type": "forecast",
    "name": "天気",
    "enName": "WEATHER",
    "priority": 1
  },
  {
    "type": "observation",
    "name": "気象観測",
    "enName": "OBSERVATION",
    "priority": 2
  },
  {
    "type": "ocean",
    "name": "海洋",
    "enName": "MARINE",
    "priority": 3
  },
  {
    "type": "earth",
    "name": "地震・津波",
    "enName": "EARTH QUAKE",
    "priority": 4
  },
  {
    "type": "volcano",
    "name": "火山",
    "enName": "VOLCANO",
    "priority": 5
  }
]
```

### `[.contents[]|select(.type=="bousai")]`

```json
[
  {
    "id": "bosaitop",
    "icon": "common/image/bosai_home.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "あなたの街の防災情報",
    "enName": "Local Information",
    "kana": "あなたのまちのぼうさいじょうほう",
    "keywords": [
      "あなたのまち",
      "ぼうさい",
      "じょうほう"
    ],
    "url": "",
    "enUrl": "#lang=en",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "warning",
    "icon": "common/image/bosai_warning.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "気象警報・注意報",
    "enName": "Weather Warnings/Advisories",
    "kana": "きしょうけいほうちゅういほう",
    "keywords": [
      "きしょう",
      "けいほう",
      "ちゅういほう"
    ],
    "url": "map.html#contents=warning",
    "enUrl": "map.html#contents=warning&lang=en",
    "mapValue": "warning",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    }
  },
  {
    "id": "warning_level",
    "icon": "common/image/bosai_warning_level.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "大雨危険度",
    "kana": "おおあめきけんど",
    "keywords": [
      "おおあめ",
      "きけんど"
    ],
    "url": "map.html#contents=warning_level",
    "mapValue": "warning_level",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    }
  },
  {
    "id": "risk_map",
    "icon": "common/image/bosai_weathermesh.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "危険度分布",
    "enName": "Risk Map",
    "kana": "きけんどぶんぷ",
    "keywords": [
      "きけんど",
      "ぶんぷ"
    ],
    "url": "risk/",
    "enUrl": "en_risk/",
    "mapValue": "nishimura_contents",
    "priority": 0,
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    },
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "typhoon",
    "icon": "common/image/bosai_typhoon.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "台風情報",
    "enName": "Tropical Cyclone Information",
    "kana": "たいふうじょうほう",
    "keywords": [
      "たいふう",
      "じょうほう"
    ],
    "url": "map.html#contents=typhoon&elem=typhoon_all",
    "enUrl": "map.html#contents=typhoon&elem=typhoon_all&lang=en",
    "mapValue": "typhoon",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "information",
    "icon": "common/image/bosai_information.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "気象情報",
    "kana": "きしょうじょうほう",
    "keywords": [
      "きしょう",
      "じょうほう"
    ],
    "url": "map.html#contents=information",
    "enUrl": "map.html#contents=information&lang=en",
    "mapValue": "information",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "offices"
    }
  },
  {
    "id": "tornado",
    "icon": "common/image/bosai_tornado.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "竜巻注意情報",
    "enName": "Hazardous Wind Watch",
    "kana": "たつまきちゅういじょうほう",
    "keywords": [
      "たつまき",
      "ちゅうい",
      "じょうほう"
    ],
    "url": "map.html#element=tornado&contents=information",
    "enUrl": "map.html#element=tornado&contents=information&lang=en",
    "mapValue": "information&element=tornado",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    }
  },
  {
    "id": "kirokuame",
    "icon": "common/image/bosai_rain02.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "記録的短時間大雨情報",
    "enName": "Heavy Rain Information",
    "kana": "きろくてきたんじかんおおあめじょうほう",
    "keywords": [
      "きろく",
      "たんじかん",
      "おおあめ",
      "じょうほう"
    ],
    "url": "map.html#element=kirokuame&contents=information",
    "enUrl": "map.html#element=kirokuame&contents=information&lang=en",
    "mapValue": "information&element=kirokuame",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "offices"
    }
  },
  {
    "id": "high-temp",
    "icon": "common/image/bosai_high_temp.svg",
    "type": "bousai",
    "context": "jdds",
    "name": "高温注意情報",
    "enName": "Extreme High Temperature Forecasts",
    "kana": "こうおんちゅういじょうほう",
    "keywords": [
      "こうおん",
      "ちゅうい",
      "じょうほう"
    ],
    "url": "//www.data.jma.go.jp/fcd/yoho/data/kouon/",
    "enUrl": "//www.data.jma.go.jp/fcd/yoho/data/kouon/index_en.html",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "flood",
    "icon": "common/image/bosai_flood.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "指定河川洪水予報",
    "kana": "していかせんこうずいよほう",
    "keywords": [
      "してい",
      "かせん",
      "こうずい",
      "よほう"
    ],
    "url": "flood/",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    }
  },
  {
    "id": "floodindex",
    "icon": "common/image/bosai_floodindex.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "流域雨量指数",
    "kana": "りゅういきうりょうしすう",
    "keywords": [
      "りゅういき",
      "うりょう",
      "しすう"
    ],
    "url": "floodindex/",
    "priority": 0,
    "realm": [
      "develop",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    }
  },
  {
    "id": "rain",
    "icon": "common/image/bosai_rain.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "雨雲の動き",
    "enName": "High-resolution Precipitation Nowcasts",
    "kana": "あまぐものうごき",
    "keywords": [
      "あまぐもの",
      "うごき"
    ],
    "url": "nowc/",
    "enUrl": "en_nowc/",
    "mapValue": "nishimura_contents",
    "priority": 0,
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    },
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "rain_analysis",
    "icon": "common/image/bosai_rain.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "今後の雨",
    "enName": "Analysis and Forecast of Precipitation",
    "kana": "こんごのあめ",
    "keywords": [
      "こんごの",
      "あめ"
    ],
    "url": "kaikotan/",
    "enUrl": "en_kaikotan/",
    "mapValue": "nishimura_contents",
    "priority": 0,
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    },
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "snow",
    "icon": "common/image/bosai_yukimesh.svg",
    "type": "bousai",
    "context": "bosai",
    "name": "現在の雪",
    "enName": "Snow Analysis",
    "kana": "げんざいのゆき",
    "keywords": [
      "げんざいの",
      "ゆき"
    ],
    "url": "snow/",
    "enUrl": "en_snow/",
    "mapValue": "nishimura_contents",
    "priority": 0,
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    },
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  }
]
```

### `[.contents[]|select(.type=="forecast")]`

```json
[
  {
    "id": "forecast",
    "icon": "common/image/bosai_forecast.svg",
    "type": "forecast",
    "context": "bosai",
    "name": "天気予報",
    "enName": "Daily Forecasts",
    "kana": "てんきよほう",
    "keywords": [
      "てんき",
      "よほう"
    ],
    "url": "map.html#contents=forecast",
    "enUrl": "map.html#contents=forecast&lang=en",
    "mapValue": "forecast",
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    },
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "forecast_map",
    "icon": "common/image/bosai_wdist.svg",
    "type": "forecast",
    "context": "bosai",
    "name": "天気分布予報",
    "enName": "Distribution Forecasts",
    "kana": "てんきぶんぷよほう",
    "keywords": [
      "てんきぶんぷ",
      "よほう"
    ],
    "url": "wdist/",
    "enUrl": "en_wdist/",
    "mapValue": "nishimura_contents",
    "priority": 0,
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    },
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "three_hourly_forecasts",
    "icon": "common/image/bosai_soukei.svg",
    "type": "forecast",
    "context": "bosai",
    "name": "地域時系列予報",
    "enName": "Three-hourly Forecasts",
    "kana": "ちいきじけいれつよほう",
    "keywords": [
      "ちいき",
      "じけいれつ"
    ],
    "url": "wdist/timeseries.html",
    "enUrl": "en_wdist/timeseries.html",
    "mapValue": "nishimura_contents",
    "priority": 0,
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    },
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "2week-forecast",
    "icon": "common/image/bosai_2week_forecast.svg",
    "type": "forecast",
    "context": "jdds",
    "name": "２週間気温予報",
    "enName": "Two-week Temperature Forecast",
    "kana": "２しゅうかんきおんよほう",
    "keywords": [
      "２しゅうかん",
      "きおん",
      "よほう"
    ],
    "url": "//www.data.jma.go.jp/gmd/cpd/twoweek/",
    "enUrl": "//www.data.jma.go.jp/gmd/cpd/twoweek/en/",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "soukei",
    "icon": "common/image/bosai_soukei.svg",
    "type": "forecast",
    "context": "jdds",
    "name": "早期天候情報",
    "enName": "Early Warning Information on Extreme Weather",
    "kana": "そうきてんこうじょうほう",
    "keywords": [
      "そうき",
      "てんこう",
      "じょうほう"
    ],
    "url": "//www.data.jma.go.jp/gmd/cpd/souten/",
    "enUrl": "//www.data.jma.go.jp/gmd/cpd/souten/en/",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "season",
    "icon": "common/image/bosai_season.svg",
    "type": "forecast",
    "context": "bosai",
    "name": "季節予報",
    "enName": "Seasonal Forecasts",
    "kana": "きせつよほう",
    "keywords": [
      "きせつ",
      "よほう"
    ],
    "url": "map.html#contents=season",
    "enUrl": "map.html#contents=season&lang=en",
    "mapValue": "season",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "offices"
    }
  },
  {
    "id": "weather-map",
    "icon": "common/image/bosai_weather_map.svg",
    "type": "forecast",
    "context": "bosai",
    "name": "天気図",
    "enName": "Weather Maps",
    "kana": "てんきず",
    "keywords": [
      "てんきず"
    ],
    "url": "weather_map/",
    "enUrl": "weather_map/#lang=en",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "uv",
    "icon": "common/image/bosai_uvidx.svg",
    "type": "forecast",
    "context": "jdds",
    "name": "紫外線",
    "enName": "UV Index",
    "kana": "しがいせん",
    "keywords": [
      "しがいせん",
      "uv"
    ],
    "url": "//www.data.jma.go.jp/gmd/env/uvindex/",
    "enUrl": "//www.data.jma.go.jp/gmd/env/uvindex/en/",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "kosa",
    "icon": "common/image/bosai_kosa.svg",
    "type": "forecast",
    "context": "jdds",
    "name": "黄砂",
    "enName": "Aeolian Dust Information",
    "kana": "こうさ",
    "keywords": [
      "こうさ"
    ],
    "url": "//www.data.jma.go.jp/gmd/env/kosa/fcst/",
    "enUrl": "//www.data.jma.go.jp/gmd/env/kosa/fcst/en/",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  }
]
```

### `[.contents[]|select(.type=="observation")]`

```json
[
  {
    "id": "himawari",
    "icon": "common/image/bosai_himawari.svg",
    "type": "observation",
    "context": "bosai",
    "name": "ひまわり",
    "enName": "Satellite Imagery",
    "kana": "ひまわり",
    "keywords": [
      "ひまわり",
      "衛星"
    ],
    "url": "map.html#elem=ir&contents=himawari",
    "enUrl": "map.html#elem=ir&contents=himawari&lang=en",
    "mapValue": "himawari",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "amedas",
    "icon": "common/image/bosai_amedas1h.svg",
    "type": "observation",
    "context": "bosai",
    "name": "アメダス",
    "enName": "Weather Observations",
    "kana": "あめだす",
    "keywords": [
      "あめだす"
    ],
    "url": "map.html#elem=temp&contents=amedas",
    "enUrl": "map.html#elem=temp&contents=amedas&lang=en",
    "mapValue": "amedas",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    }
  },
  {
    "id": "suikei_kishou_bunpu",
    "icon": "common/image/bosai_wdist.svg",
    "type": "observation",
    "context": "jdds",
    "name": "推計気象分布",
    "enName": "Weather Analysis Map",
    "kana": "すいけいきしょうぶんぷ",
    "keywords": [
      "すいけい",
      "きしょうぶんぷ"
    ],
    "url": "//www.data.jma.go.jp/obd/bunpu/",
    "enUrl": "//www.data.jma.go.jp/obd/bunpu/index_en.html",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "windprofiler",
    "icon": "common/image/bosai_windprofiler.svg",
    "type": "observation",
    "context": "bosai",
    "name": "ウィンドプロファイラ",
    "kana": "うぃんどぷろふぁいら",
    "keywords": [
      "うぃんど",
      "ぷろふぁいら"
    ],
    "url": "map.html#contents=windprofiler",
    "mapValue": "windprofiler",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    }
  }
]
```

### `[.contents[]|select(.type=="ocean")]`

```json
[
  {
    "id": "seawarning",
    "icon": "common/image/bosai_seawarning.svg",
    "type": "ocean",
    "context": "bosai",
    "name": "海上警報・予報",
    "enName": "Marine Warnings/Forcasts",
    "kana": "かいじょうけいほうよほう",
    "keywords": [
      "かいじょう",
      "けいほう",
      "よほう"
    ],
    "url": "map.html#contents=seawarning",
    "enUrl": "map.html#contents=seawarning&lang=en",
    "mapValue": "seawarning",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "umimesh",
    "icon": "common/image/bosai_umimesh.svg",
    "type": "ocean",
    "context": "bosai",
    "name": "海上分布予報",
    "enName": "Distribution Marine Forecasts",
    "kana": "かいじょうぶんぷよほう",
    "keywords": [
      "かいじょう",
      "ぶんぷ",
      "よほう"
    ],
    "url": "umimesh/",
    "enUrl": "en_umimesh/",
    "mapValue": "nishimura_contents",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "tidelevel",
    "icon": "common/image/bosai_tide_height.svg",
    "type": "ocean",
    "context": "bosai",
    "name": "潮位観測情報",
    "kana": "ちょういかんそくじょうほう",
    "keywords": [
      "ちょうい",
      "かんそく",
      "じょうほう"
    ],
    "url": "map.html#contents=tidelevel",
    "mapValue": "tidelevel",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    }
  },
  {
    "id": "waveinf",
    "icon": "common/image/bosai_wave.svg",
    "type": "ocean",
    "context": "jdds",
    "name": "波浪実況・予想図",
    "enName": "Sea Waves",
    "kana": "はろうじっきょう・よそうず",
    "keywords": [
      "はろう",
      "じっきょう",
      "よそうず"
    ],
    "url": "//www.data.jma.go.jp/gmd/waveinf/tile/jp/",
    "enUrl": "//www.data.jma.go.jp/gmd/waveinf/chart/awjp_e.html",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "wave",
    "icon": "common/image/bosai_wave.svg",
    "type": "ocean",
    "context": "bosai",
    "name": "波浪観測情報",
    "kana": "はろうかんそくじょうほう",
    "keywords": [
      "はろう",
      "かんそく",
      "じょうほう"
    ],
    "url": "map.html#&contents=wave",
    "mapValue": "wave",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  }
]
```

### `[.contents[]|select(.type=="earth")]`

```json
[
  {
    "id": "tsunami",
    "icon": "common/image/bosai_tsunami.svg",
    "type": "earth",
    "context": "bosai",
    "name": "津波",
    "enName": "Tsunami Warnings/Advisories",
    "kana": "つなみ",
    "keywords": [
      "つなみ"
    ],
    "url": "map.html#contents=tsunami&elem=warn",
    "enUrl": "map.html#contents=tsunami&elem=warn&lang=en",
    "mapValue": "tsunami",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "earthquake_map",
    "icon": "common/image/bosai_earthquake.svg",
    "type": "earth",
    "context": "bosai",
    "name": "地震情報",
    "enName": "Earthquake Information",
    "kana": "じしんじょうほう",
    "keywords": [
      "じしん",
      "じょうほう"
    ],
    "url": "map.html#contents=earthquake_map",
    "enUrl": "map.html#contents=earthquake_map&lang=en",
    "mapValue": "earthquake_map",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    }
  },
  {
    "id": "estimated_intensity_map",
    "icon": "common/image/bosai_estimated_intensity_map.svg",
    "type": "earth",
    "context": "bosai",
    "name": "推計震度分布",
    "kana": "すいけいしんどぶんぷ",
    "keywords": [
      "すいけい",
      "しんど",
      "ぶんぷ"
    ],
    "url": "map.html#contents=estimated_intensity_map",
    "mapValue": "estimated_intensity_map",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "class20s"
    }
  },
  {
    "id": "tyoushuuki",
    "icon": "common/image/bosai_tyoushuuki.svg",
    "type": "earth",
    "context": "jdds",
    "name": "長周期地震動",
    "kana": "ちょうしゅうきじしんどう",
    "keywords": [
      "ちょうしゅうき",
      "じしんどう"
    ],
    "url": "//www.data.jma.go.jp/svd/eew/data/ltpgm/",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "nteq",
    "icon": "common/image/bosai_nteq.svg",
    "type": "earth",
    "context": "bosai",
    "name": "南海トラフ地震",
    "kana": "なんかいとらふ",
    "keywords": [
      "なんかい",
      "とらふ"
    ],
    "url": "nteq",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  },
  {
    "id": "hypo",
    "icon": "common/image/bosai_hypo.svg",
    "type": "earth",
    "context": "bosai",
    "name": "震央分布",
    "kana": "しんおうぶんぷじょうほう",
    "keywords": [
      "しんおう",
      "ぶんぷ"
    ],
    "url": "map.html#contents=hypo",
    "mapValue": "hypo",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ]
  }
]
```

### `[.contents[]|select(.type=="volcano")]`

```json
[
  {
    "id": "volcano",
    "icon": "common/image/bosai_volcano.svg",
    "type": "volcano",
    "context": "bosai",
    "name": "噴火警報・噴火速報",
    "enName": "Volcanic Warnings",
    "kana": "ふんかけいほう・ふんかそくほう",
    "keywords": [
      "ふんか",
      "けいほう",
      "そくほう"
    ],
    "url": "map.html#contents=volcano",
    "enUrl": "map.html#contents=volcano&lang=en",
    "mapValue": "volcano",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "offices"
    }
  },
  {
    "id": "ashfall",
    "icon": "common/image/bosai_ashfall.svg",
    "type": "volcano",
    "context": "bosai",
    "name": "降灰予報",
    "enName": "Volcanic Ash Fall Forecasts",
    "kana": "こうはいよほう",
    "keywords": [
      "こうはい",
      "よほう"
    ],
    "url": "map.html#contents=ashfall",
    "enUrl": "map.html#contents=ashfall&lang=en",
    "mapValue": "ashfall",
    "priority": 0,
    "realm": [
      "develop",
      "bosai",
      "example",
      "test"
    ],
    "areaHandover": {
      "japan": "japan",
      "offices": "offices",
      "class20s": "offices"
    }
  }
]
```



## 情報源

- [ツイ](https://twitter.com/izutorishima/status/1364441626672685058)

> まじかよ気象庁公式の天気予報APIができてるぞ、感激して大声で泣いちゃった<https://t.co/2HQumqjel8>
>  &mdash; Torishima (@izutorishima)[February 24, 2021](https://twitter.com/izutorishima/status/1364441626672685058?ref_src=twsrc%5Etfw)

- [気象庁ホームページ防災気象情報のURL構造 - Qiita](https://qiita.com/e_toyoda/items/7a293313a725c4d306c0)
