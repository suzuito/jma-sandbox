NPM_BIN ?= ../node_modules/.bin
SIMPLIFY ?= 10

out:
	mkdir -p out

out/全国・地方予報区等.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaForecast_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/全国・地方予報区等.geojson: out/全国・地方予報区等.shp
	$(NPM_BIN)/mapshaper out/全国・地方予報区等.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/府県予報区等.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaForecastLocalM_prefecture_GIS.zip -o $@
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/府県予報区等.geojson: out/府県予報区等.shp
	$(NPM_BIN)/mapshaper out/府県予報区等.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/一次細分区域等.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaForecastLocalM_1saibun_GIS.zip -o $@
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/一次細分区域等.geojson: out/一次細分区域等.shp
	$(NPM_BIN)/mapshaper out/一次細分区域等.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/市町村等をまとめた地域等: out/
	curl -o $@.zip -LO https://www.data.jma.go.jp/developer/gis/20200526_AreaForecastLocalM_matome_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $@.zip out/
out/市町村等をまとめた地域等.geojson: out/市町村等をまとめた地域等
	$(NPM_BIN)/mapshaper out/市町村等をまとめた地域等/市町村等をまとめた地域等.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/市町村等（気象警報等）:
	curl -o $@.zip -LO https://www.data.jma.go.jp/developer/gis/20200526_AreaInformationCity_weather_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $@.zip out/
out/市町村等（気象警報等）.geojson: out/市町村等（気象警報等）
	$(NPM_BIN)/mapshaper out/市町村等（気象警報等）/市町村等（気象警報等）.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/市町村等（土砂災害警戒情報）: out/
	curl -o $@.zip -LO https://www.data.jma.go.jp/developer/gis/20200526_AreaInformationCity_landslide_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $@.zip out/
out/市町村等（土砂災害警戒情報）.geojson: out/市町村等（土砂災害警戒情報）
	$(NPM_BIN)/mapshaper out/市町村等（土砂災害警戒情報）/市町村等（土砂災害警戒情報）.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/20190508_AreaInformationCity_river_GIS: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190508_AreaInformationCity_river_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/市町村等（指定河川洪水予報）.geojson: out/20190508_AreaInformationCity_river_GIS
	$(NPM_BIN)/mapshaper out/20190508_AreaInformationCity_river_GIS/市町村等（指定河川洪水予報）.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/市町村等（地震津波関係）.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaInformationCity_quake_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/市町村等（地震津波関係）.geojson: out/市町村等（地震津波関係）.shp
	$(NPM_BIN)/mapshaper out/市町村等（地震津波関係）.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/市町村等（火山関係）.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaInformationCity_volcano_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/市町村等（火山関係）.geojson: out/市町村等（火山関係）.shp
	$(NPM_BIN)/mapshaper out/市町村等（火山関係）.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/地方海上予報区.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaMarineAJ_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/地方海上予報区.geojson: out/地方海上予報区.shp
	$(NPM_BIN)/mapshaper out/地方海上予報区.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/緊急地震速報／地方予報区.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaForecastEEW_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/緊急地震速報／地方予報区.geojson: out/緊急地震速報／地方予報区.shp
	$(NPM_BIN)/mapshaper out/緊急地震速報／地方予報区.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/緊急地震速報／府県予報区.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaForecastLocalEEW_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/緊急地震速報／府県予報区.geojson: out/緊急地震速報／府県予報区.shp
	$(NPM_BIN)/mapshaper out/緊急地震速報／府県予報区.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/地震情報／都道府県等.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaInformationPrefectureEarthquake_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/地震情報／都道府県等.geojson: out/地震情報／都道府県等.shp
	$(NPM_BIN)/mapshaper out/地震情報／都道府県等.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/地震情報／細分区域.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaForecastLocalE_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/地震情報／細分区域.geojson: out/地震情報／細分区域.shp
	$(NPM_BIN)/mapshaper out/地震情報／細分区域.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@

out/津波予報区.shp: out/
	curl -o $(basename $@).zip -LO https://www.data.jma.go.jp/developer/gis/20190125_AreaTsunami_GIS.zip
	ditto -V -x -k --sequesterRsrc --rsrc $(basename $@).zip out/
out/津波予報区.geojson: out/津波予報区.shp
	$(NPM_BIN)/mapshaper out/津波予報区.shp encoding=utf-8 -simplify $(SIMPLIFY)% -o $@


clean:
	rm -rf out