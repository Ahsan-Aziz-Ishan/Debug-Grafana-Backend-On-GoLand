# Debug-Grafana-Backend-On-GoLand
# If you want, you can buy me a pizza [here](https://buymeacoffee.com/portmafia9719) (if this works,as you know this wasn't really really easy ) 

# Make sure you have the latest/compatible version of delve in GoLand
From Command Line:
```
go run build.go setup
go run build.go build
```

# Enable CGO with CGO_ENABLED=1
*******************************************************************************************
<img width="998" alt="image" src="https://github.com/Ahsan-Aziz-Ishan/Debug-Grafana-Backend-On-GoLand/assets/101202264/f8e7de16-23db-45b4-b109-3df10a5520a2">


Goland new Run Config
*******************************************************************************************
**Run Kind:** `Package`

**Package Path:** `github.com/grafana/grafana/pkg/cmd/grafana`

[x] Run after Build

**Working Directory:** `<downloaded repo root path>`

**Environment:** `PATH=$PATH:<downloaded repo root path>/bin/darwin-amd64/:/usr/bin/`.

^^note: `darwin-amd64` is for mac-os, change as per need, or where your binaries are generated inside the `<downloaded repo root path>/bin` folder . `/usr/bin/` because it depends on clang

**Go too arguments:**  `-trimpath`

**Program Arguments:** `server -packaging=dev cfg:app_mode=development`

<img width="1344" alt="image" src="https://github.com/Ahsan-Aziz-Ishan/Debug-Grafana-Backend-On-GoLand/assets/101202264/9da2ca6d-793e-4ead-b7f9-2cbe9b3d0941">
