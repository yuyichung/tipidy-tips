# Golang

- Updating Revel after installing a new version of Golang:
  - rm -rf /REVEL_PATH/bin/revel
  - rm -rf /REVEL_PATH/pkg/*
  - go install revel
- Print something in JSON format:
  - import "encoding/json" and "os"
  - encoder := json.NewEncoder(os.Stdout)
  - encoder.Encode(obj)