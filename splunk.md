- timechart by multiple fields: index=myindex earliest=-50d \| eval fieldaplusb= fielda + ":" + fieldb \| timechart count by fieldaplusb useother=false usenull=false

