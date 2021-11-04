# atxserver2-ios-provider
Apple device provider for atxserver2. iOS real device

## Requirements
- Python >= 3.6
- WebDriverAgent(appium)
- NodeJS 8

## Install
set libimobiledevice tools

```bash
brew uninstall --ignore-dependencies libimobiledevice
brew uninstall --ignore-dependencies usbmuxd

brew install --HEAD usbmuxd
brew unlink usbmuxd
brew link usbmuxd

brew install --HEAD libimobiledevice
brew install ideviceinstaller
brew link --overwrite ideviceinstaller
```

setup atxserver2-ios-provider, iOS real device  need ATX-WebDriverAgent pre-installed on the device

```bash
git clone https://github.com/openatx/atxserver2-ios-provider
cd atxserver2-ios-provider

# install dependencies
pip3 install -r requirements.txt
npm install # ensure NodeJS 8 is used, higher version node doesn't work
```

setup rtcsrv which  need go 1.16 or higher
```
cd $GOPATH/src
git clone git@gitlab.myteksi.net:kui.chen/rtcsrv.git
cd $GOPATH/src/rtcsrv
go build && go install
```

# LICENSE
[MIT](LICENSE)



python3 main.py  --use-tidevice 