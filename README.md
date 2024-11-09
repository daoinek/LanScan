# LanScan

A simple library to scan the current Wi-Fi network and get the IP addresses of connected devices.

## Installation

Swift Package Manager

- File > Swift Packages > Add Package Dependency
- Add https://github.com/daoinek/LanScan.git

## Usage

Before use, import the library using `import LanScan`

```swift
var scanner: LanScan?

scanner = LanScan(delegate: self)
scanner?.start()
scanner?.stop()


//MARK: LAN Delegate
func lanScanHasUpdatedProgress(_ counter: Int, address: String!) {}
func lanScanDidFindNewDevice(_ device: [AnyHashable : Any]!) {}
func lanScanDidFinishScanning() {}
```
