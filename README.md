# jma-sandbox

要件

- MacOS
- nodejs

セットアップ

```bash
npm install
```

## GIS

[気象庁のGISデータ](https://www.data.jma.go.jp/developer/gis.html)をGeoJSONとして取得します。

使い方

```bash
make clean
make out/全国・地方予報区等.geojson
make out/府県予報区等.geojson
make out/一次細分区域等.geojson
make out/市町村等をまとめた地域等.geojson
make out/市町村等（気象警報等）.geojson
make out/市町村等（土砂災害警戒情報）.geojson
make out/市町村等（指定河川洪水予報）.geojson
make out/市町村等（地震津波関係）.geojson
make out/市町村等（火山関係）.geojson
make out/地方海上予報区.geojson
make out/緊急地震速報／地方予報区.geojson
make out/地震情報／都道府県等.geojson
make out/地震情報／細分区域.geojson
make out/津波予報区.geojson
```

```bash
curl -LO https://www.data.jma.go.jp/developer/gis/20200526_AreaForecastLocalM_matome_GIS.zip
```
